# OpenPortEx Method - intrepidcs API

_This function is deprecated. Use the_ [_OpenNeoDevice_](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) _method instead._

This function opens a connection to a neoVI device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoOpenPortEx( int lPortNumber, int lPortType, int lDriverType, int lIPAddressMSB, int lIPAddressLSBOrBaudRate, int bConfigRead, unsigned char * bNetworkID, int * hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoOpenPortEx Lib “icsneo40.dll” (ByVal lPortNumber As Integer, ByVal lPortType As Integer, ByVal lDriverID As Integer, ByVal lIPAddressMSB As Integer, ByVal lIPAddressLSBOrBaudRate As Integer, ByVal lForceConfigRead As Integer, ByRef bNetworkID As Byte, ByRef hObject As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoOpenPortEx(int lPortNumber, int lPortType, int lDriverID,int lIPAddressMSB, int lIPAddressLSBOrBaudRate, int lForceConfigRead, ref byte bNetworkID,ref int hObject);
```
{% endtab %}
{% endtabs %}

**Parameters**

lPortNumber

\[in] Specifies which USB, TCP/IP, or Comm port to use. The USB port is a logic port starting with 1 up to the number of devices. For example, if 3 devices are connected, valid lPortNumber values will be 1,2, and 3. Comm ports also start at 1. For TCP/IP it specifies the TCP/IP port number.

lPortType

\[in] Specifies the port type of what the device is connected to. This parameter is used with lPortNumber described above. This parameter can be set to NEOVI\_COMMTYPE\_RS232 (0) for a RS232 Comm port, NEOVI\_COMMTYPE\_USB\_BULK (1) for a USB, or NEOVI\_COMMTYPE\_TCPIP (3) for a TCP/IP connection. More information on the different types of hardware and the connection it uses can be found in the [OpenPortEx Hardware Type](openportex-hardware-type-information-intrepidcs-api.md) help topic.

lDriverType

\[in] Specifies which neoVI driver to use. This should always be set to INTREPIDCS\_DRIVER\_STANDARD (0).

lIPAddressMSB

\[in] Specifies upper two bytes of TCP/IP address if the lPortType is set to NEOVI\_COMMTYPE\_TCPIP (bytes 4 and 3 of this TCP/IP address: 1.2.3.4).

lIPAddressLSBOrBaudRate

\[in] Specifies the baud rate if lPortType is NEOVI\_COMMTYPE\_RS232 and the lower two bytes of the TCP/IP address (bytes 2 and 1 of this TCP/IP address: 1.2.3.4).

bConfigRead

\[in] Specifies whether the DLL should read the configuration before enabling the device. It is recommended to set this value to 1. This parameter is ignored when the object is created because the configuration is read by default.

bNetworkIDs

\[in] This is an array of number IDs which specify the NetworkID parameter of each network. This allows you to assign a custom network ID to each network. Normally, you will assign consecutive IDs to each of the networks. The network IDs are specified in the following list: NETID\_DEVICE = 0, NETID\_HSCAN = 1, NETID\_MSCAN = 2, NETID\_SWCAN = 3, NETID\_LSFTCAN = 4, NETID\_FORDSCP = 5, NETID\_J1708 = 6, NETID\_AUX = 7, NETID\_JVPW = 8, NETID\_ISO = 9. _**You may also set this parameter to NULL (zero) and the default network ID’s will be used.**_

The neoVI DLL will use this array when it receives a network message. For example, when the DLL receives a message from HSCAN network it will set the NetworkID parameter of the [message structure](../../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/message-structures-neovi-api.md) with the value bNetworkID(NETID\_HSCAN).

hObject

\[in, out] This is the handle of the neoVI driver object. If this handle is 0, the method will create a new neoVI driver object. This handle will be used in other neoVI API calls to read and transmit messages.

Every time you create a new neoVI driver object you must call [icsneoFreeObject](../../basic-functions-overview-intrepidcs-api/freeobject-method-intrepidcs-api.md) (after [ClosePort](../../basic-functions-overview-intrepidcs-api/closeport-method-intrepidcs-api.md)). If you do not you will create a memory leak.

**Return Values**

If the port has been opened successfully and connection to neoVI is attained, the return value will be 1. If the function fails the return value will be zero. The most common reason for failure is when the neoVI is not connected to the port described in the parameters.

**Remarks**

Each successful call to OpenPort should be matched with a call to [ClosePort](../../basic-functions-overview-intrepidcs-api/closeport-method-intrepidcs-api.md). The OpenPort call will reset the timestamp clock.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
unsigned char bNetworkID[16];     // array of network ids
int hObject = 0;         // holds a handle to the neoVI object
unsigned long lCount;            // counter variable
int iIPLSB;
int iIPMSB;

// initialize the networkid array
for (lCount=0;lCount<16;lCount++)
    bNetworkID[lCount] = lCount;


if (!m_bPortOpen) // only if not already opened
{
    iIPLSB = 57600;
    iIPMSB = 0;

    lResult = icsneoOpenPortEx(1 ,NEOVI_COMMTYPE_RS232,INTREPIDCS_DRIVER_STANDARD,iIPMSB,iIPLSB,1,bNetworkID,&hObject);
    if (lResult == 0)
        MessageBox(hWnd,TEXT("Problem Opening Port"),TEXT("neoVI Example"),0);
    else
    {
        m_bPortOpen =true;
        MessageBox(hWnd,TEXT("Port Opened Successfully"),TEXT("neoVI Example"),0);
    }
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim lResult As Long
Dim iIPMSB As Integer
Dim iIPLSB As Integer

iIPMSB = 0
iIPLSB = 0
lResult = 0

''command To Open up the port
If optUsbDevice.Checked = False Then
    iIPLSB = 57600  ''Set Baud Rate for Serial Communication
    lResult = icsneoOpenPortEx(Val(txtCommPortNum.Text), NEOVI_COMMTYPE_RS232, _
        INTREPIDCS_DRIVER_STANDARD, iIPMSB, iIPLSB, 1, NETID_HSCAN, m_hObject)
Else
    lResult = icsneoOpenPortEx(Val(txtCommPortNum.Text), NEOVI_COMMTYPE_USB_BULK, _
            INTREPIDCS_DRIVER_STANDARD, iIPMSB, iIPLSB, 1, NETID_HSCAN, m_hObject)
End If

''Check the status of the opened port
If CBool(lResult) Then
    MsgBox("Port Opened OK!")
Else
    MsgBox("Problem Opening Port")
End If
m_bPortOpen = True
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
byte bNetworkIDs = 1;
int iPortNumber = 0;
int iReturnVal = 0; //iReturn value tells status of the function call
int iIPMSB = 0;
int iIPLSB = 0;

iPortNumber = Convert.ToInt32( txtCommPortNum.Text); //Convert type of Textbox Value
//Open the Device on the Port indicated in the Text box
if(optUsbDevice.Checked == false)
{
    iIPLSB = 57600;
    iReturnVal = icsNeoDll.icsneoOpenPortEx(iPortNumber, Convert.ToInt32(ePORT_TYPE.NEOVI_COMMTYPE_RS232),
        Convert.ToInt32(eDRIVER_TYPE.INTREPIDCS_DRIVER_STANDARD),iIPMSB ,iIPLSB,1, ref bNetworkIDs,     ref m_hObject);
}
else
{
    iReturnVal = icsNeoDll.icsneoOpenPortEx(iPortNumber, Convert.ToInt32(ePORT_TYPE.NEOVI_COMMTYPE_USB_BULK ),
        Convert.ToInt32(eDRIVER_TYPE.INTREPIDCS_DRIVER_STANDARD),iIPMSB , iIPLSB, 1, ref    bNetworkIDs,ref m_hObject);
}

if (iReturnVal == 0) // test the returned result
{
    MessageBox.Show("Problem Opening Port"); //Error, Show message
}
else
{
    MessageBox.Show("Port opened OK!");
    m_bPortOpen = true; //Set Port Opened Flag
}
```
{% endtab %}
{% endtabs %}
