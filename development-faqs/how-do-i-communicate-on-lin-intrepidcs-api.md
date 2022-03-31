# How do I communicate on LIN - intrepidcs API

The very first step to working with LIN is to make sure it is enabled on your hardware device. This is done in neoVI Explorer. Please see the hardware documentation for the device to be used on how to do this.

Working with LIN can be done in different ways, so it is important to know how what is needed for the LIN network that is being connected to. Is the application going to act as a Master, Slave, or just spy on the bus? If just spying on the bus is needed, messages can be read like other networks.

The first step to acting as a Master is to enable the Master resistor in the hardware. This is done in neoVI Explorer under the desired LIN channel. This is not needed if the cabling includes the resistor or when operating as a Slave. Below is the setup for a simple Master request with no slave data. Note that the J1850 Spy Message structure is used and the LIN protected ID is in the first data byte.

**Master frame no slave Data**

```
//Use J1850 Message structure
//This breaks the ARBID into 4 bytes
icsSpyMessageJ1850 stJMsg;
long lNetworkID;

//Set the Network ID
lNetworkID = NETID_LIN; //16 for LIN1
//Set the LIN ID, use the Protected ID
stJMsg.Header[0] = 0xf0; 
//Set the Number of Databytes to 0
stJMsg.NumberBytesData = 0;

//Set the Init Message flag. This tells the
//Hardware that this is a Master frame
stJMsg.StatusBitField=SPY_STATUS_INIT_MESSAGE;
stJMsg.StatusBitField2=0; 
//Set the number of Header bytes to 1
stJMsg.NumberBytesHeader = 1;

//Send the message
lResult = icsneoTxMessages(m_hObject, (icsSpyMessage * )&stJMsg, lNetworkID, 1);

```

**Master frame with Slave data**

```
//Use J1850 Message structure
//This breaks the ARBID into 4 bytes
icsSpyMessageJ1850 stJMsg;
long lNetworkID;

//Set the Network ID
lNetworkID = NETID_LIN; //16 for LIN1
//Set the LIN ID, use the Protected ID
stJMsg.Header[0] = 0x30; 

//Set the Number of Header bytes to 3
//The first 2 data bytes go in the Header section.
stJMsg.NumberBytesHeader = 3;

stJMsg.Header[1] =0x11;
stJMsg.Header[2] =0x22;
// for all the data bytes
stJMsg.Data[0] = 0x33;
stJMsg.Data[1] = 0x44;
stJMsg.Data[2] = 0x55;
stJMsg.Data[3] = 0x66;
stJMsg.Data[4] = 0x77;
stJMsg.Data[5] = 0x88;
//Checksum goes in the last byte
//This needs to be calculated to what your LIN setup uses
stJMsg.Data[6] = 0x99;

//Set the Init Message flag. This tells the
//Hardware that this is a Master frame
stJMsg.StatusBitField=SPY_STATUS_INIT_MESSAGE;
stJMsg.StatusBitField2=0; 
//Set the number of Header bytes to 1
stJMsg.NumberBytesData = 7;

//Send the message
lResult = icsneoTxMessages(m_hObject, (icsSpyMessage * )&stJMsg, lNetworkID, 1);
```

Sending a Slave message is just like sending a Master frame with Slave data. The difference is that the `SPY_STATUS_INIT_MESSAGE` bit is not set in the StatusBitField. This bit tells the hardware if the message is a Master frame or a slave frame. When sending a Slave message, it is sent and saved in the hardware. The message will be sent when a Master request is received. Once the request is received, then the Slave data goes out appended to the Master Frame. The same slave data will go out with every Master request, until a new Slave message with updated data is sent from the application to the hardware using the TxMessage function. When reading LIN, the checksum will be in the ACK1 parameter of the message structure.
