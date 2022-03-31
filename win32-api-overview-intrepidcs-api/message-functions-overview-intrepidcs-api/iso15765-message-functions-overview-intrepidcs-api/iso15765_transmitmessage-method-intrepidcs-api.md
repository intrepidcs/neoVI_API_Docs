# ISO15765\_TransmitMessage Method - intrepidcs API

**This method transmits a message using ISO15765-2 on a CAN network. icsneoISO15765\_EnableNetwroks must be called before using icsneoISO15765\_TransmitMessage. PCI bytes and Flow control decoding is taken care of by the dll for the transaction.**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
void _stdcall icsneoISO15765_TransmitMessage(void * hObject, unsigned long ulNetworkID,stCM_ISO157652_TxMessage *pMsg,unsigned long ulBlockingTimeout);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoISO15765_TransmitMessage Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByVal ulNetworkID As Integer, ByRef pMsg As stCM_ISO157652_TxMessage, ByVal ulBlockingTimeout As Integer) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoISO15765_TransmitMessage(IntPtr hObject,Int32 ulNetworkID,ref stCM_ISO157652_TxMessage pMsg,Int32 ulBlockingTimeout);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle which specifies the driver object created with the OpenPort method.

ulNetwork

\[in] Specifies the network to transmit the message on. See [NetworkID List](../../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/neovi-network-id-list.md) for a list of valid Network ID values. Network support varies by neoVI device. NETID\_DEVICE transmits on to the neoVI Device Virtual Network (see users manual).

stCM\_ISO157652\_TxMessage

\[in] This is the address of the [stCM\_ISO15765\_TxMessage](../../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/stcm\_iso157652\_txmessage-structure.md) structure. The structure contains the properties for the multi frame message transaction.

ulBlockingTimeout

\[in] Amount of time in ms to wait for flow controls before timing out.

**Return Values**

None.

**Remarks**

None.

### **Examples**

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
long lResult;
int iNetwork = 1;
int iCounter = 0;

//Create Message and adjust array to proper size
stCM_ISO157652_TxMessage tx_msg;
::ZeroMemory(&tx_msg,sizeof(stCM_ISO157652_TxMessage));
//enable ISO15765 on HS CAN
lResult = icsneoISO15765_EnableNetworks(m_hObject,NETID_HSCAN);
tx_msg.id = 0x7E0; //ArbID of the message
tx_msg.vs_netid = NETID_HSCAN; //Network to use
tx_msg.num_bytes = 64; //The number of data bytes to use
tx_msg.padding = 0xAA;//Set Padding Byte

//Set the Flags
tx_msg.flags = 0;
tx_msg.paddingEnable = true;

//Set Flow control message
tx_msg.fc_id = 0x7E8; //ArbID for the flow control Frame
tx_msg.fc_id_mask = 0xFFF; //The flow control arb filter mask (response id from receiver)
tx_msg.flowControlExtendedAddress = 0xFE; //Extended ID
tx_msg.fs_timeout = 0x100; //Flow Control Time out in ms
tx_msg.fs_wait = 0x3000; //Flow Control FS=Wait Timeout ms
tx_msg.blockSize = 0; //Block size (for sending flow Control)
tx_msg.stMin = 0;
//Fill data
for(iCounter = 0;iCounter<64;iCounter++)
{
    tx_msg.data[iCounter] = iCounter;
}

lResult = icsneoISO15765_TransmitMessage(m_hObject, NETID_HSCAN, &tx_msg, 3000);
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
int lResult;
int iCounter;
int iNetwork = 1;
byte[] DataBytes = {0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63};

//Create Message and adjust array to proper size
stCM_ISO157652_TxMessage tx_msg = new stCM_ISO157652_TxMessage();
tx_msg.data = new byte[4096];

//enable ISO15765
lResult = icsNeoDll.icsneoISO15765_EnableNetworks(m_hObject, 1);
tx_msg.id = 0x7E0; //ArbID of the message
tx_msg.vs_netid = 1; //Network to use
tx_msg.num_bytes = 64; //The number of data bytes to use
tx_msg.padding = 0xAA; //Set Padding Byte

//Set Flags
int iFlags=0;
iFlags = (iFlags | Convert.ToInt32(CSnet.stCM_ISO157652_TxMessage_Flags.paddingEnable)); //Enable Padding
tx_msg.flags = Convert.ToUInt16(iFlags);

//Set up Flow control
tx_msg.fc_id = 0x7E8; //ArbID for the flow control Frame
tx_msg.fc_id_mask = 0xFFF; //The flow control arb filter mask (response id from receiver)

tx_msg.fs_timeout = 0x100; //Flow Control Time out in ms
tx_msg.fs_wait = 0x3000; //Flow Control FS=Wait Timeout ms
tx_msg.blockSize = 0;//Block size (for sending flow Control)
tx_msg.stMin = 0;
//Fill data

for (iCounter = 0; iCounter < DataBytes.GetUpperBound(0);iCounter ++)
{
    tx_msg.data[iCounter] = DataBytes[iCounter];
}
lResult = icsNeoDll.icsneoISO15765_TransmitMessage(m_hObject, iNetwork,ref tx_msg, 3000);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim lResult As Integer
Dim iCounter As Integer
Dim iNetwork As Integer = 1
Dim DataIn() As Byte = {0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63}

'//Create Message and adjust array to proper size
Dim tx_msg As stCM_ISO157652_TxMessage
tx_msg.data = New Byte(4096) {}

'//Create Flow Control Receive filter
Dim flow_cntrl_msg As New stCM_ISO157652_RxMessage

'//enable ISO15765
lResult = icsneoISO15765_EnableNetworks(m_hObject, GetNetworkIDfromString(lstISO15765Network.Text))

tx_msg.id = &H7E0 '//ArbID of the message
tx_msg.vs_netid = NETID_HSCAN '//Network to use
tx_msg.num_bytes = 64 '//The number of data bytes to use
tx_msg.padding = &HAA '//Set Padding Byte

tx_msg.flags = 0 '//Clear Flags
tx_msg.flags = CUShort(tx_msg.flags Or stCM_ISO157652_TxMessage_Flags.paddingEnable)'//Enable Padding

'//Configure Flow Control
tx_msg.fc_id = &H7E8 '//ArbID for the flow control Frame
tx_msg.fc_id_mask = &HFFF '//The flow control arb filter mask (response id from receiver)
tx_msg.flowControlExtendedAddress = 0 '//Extended ID
tx_msg.fs_timeout = &H100 '//Flow Control Time out in ms
tx_msg.fs_wait = &H3000 '//Flow Control FS=Wait Timeout ms
tx_msg.blockSize = 0 '//Block size (for sending flow Control)
tx_msg.stMin = 0

'//Fill data
For iCounter = 0 To UBound(DataIn)
    tx_msg.data(iCounter) = DataIn(iCounter)
Next iCounter
lResult = icsneoISO15765_TransmitMessage(m_hObject, iNetwork, tx_msg, 3000)
```
{% endtab %}
{% endtabs %}
