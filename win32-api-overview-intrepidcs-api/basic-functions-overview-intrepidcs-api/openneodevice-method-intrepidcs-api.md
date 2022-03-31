---
cover: ../../.gitbook/assets/new-cover-image.png
coverY: 0
---

# OpenNeoDevice Method - IntrepidCS API

This method returns the neoVI hardware devices connected to the PC.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoOpenNeoDevice(NeoDevice *pNeoDevice, void * hObject, unsigned char *bNetworkIDs, int bConfigRead, int bSyncToPC);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoOpenNeoDevice Lib “icsneo40.dll” (ByRef pNeoDevice As NeoDevice, ByRef hObject As IntPtr, ByRef bNetworkIDs As Byte, ByVal bConfigRead As Int32, ByVal bSyncToPC As Int32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoOpenNeoDevice(ref NeoDevice pNeoDevice, ref IntPtr hObject, ref byte bNetworkIDs, Int32 bConfigRead, Int32 bSyncToPC);
```
{% endtab %}
{% endtabs %}

**Parameters**

pNeoDevice

\[in] A valid [NeoDevice](../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/neodevice-structure.md) structure filled with information about a specific neoVI device. For C++ a “void\*” can be used. For .NET, “IntPtr” is used. This must be obtained by calling [FindNeoDevices](../deprecated-functions-overview-intrepidcs-api/findneodevices-method-intrepidcs-api.md).

hObject

\[out] This parameter needs to be 32 bit in a 32 bit program and 64 bit in a 64 bit program. This will be set to the handle of the neoVI driver object that is created. It is needed as an input parameter to other API function calls. Every time you create a new neoVI object you must call [ClosePort](closeport-method-intrepidcs-api.md) and [FreeObject](freeobject-method-intrepidcs-api.md) to avoid creating a memory and resource leak.

bNetworkIDs

\[in] This is an array of number IDs which specify the NetworkID parameter of each network. This allows you to assign a custom network ID to each network. Normally, you will assign consecutive IDs to each of the networks. See [NetworkIDList](../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/neovi-network-id-list.md) for a list of current network ID’s. _ **You may also set this parameter to NULL (zero) and the default network ID’s will be used.**_

bConfigRead

> \[in] Specifies whether the DLL should read the neoVI’s device configuration before enabling the device. It is recommended that this value be set to 1.

bSyncToPC

\[in] Specifies whether timestamps for messages should be adjusted to the PC’s clock to compensate for time drift. This drift is caused by differences that occur over time between the clocks on the neoVI device and the PC.

**Return Values**

If the port has been opened successfully, the return value will be 1. Otherwise the return value will be zero.

**Remarks**

To connect to more than one piece of hardware, multiple calls to [OpenNeoDevice ](openneodevice-method-intrepidcs-api.md)can be made. The key is to provide a different [NeoDevice ](../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/neodevice-structure.md)for each device you want to open. For other function calls, use the returned hObject to talk to that device.

Each successful call to [OpenNeoDevice](openneodevice-method-intrepidcs-api.md) should be matched with a call to a [ClosePort](closeport-method-intrepidcs-api.md) when you are finished accessing the hardware. [FreeObject](freeobject-method-intrepidcs-api.md) methods.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
void * hObject;  // holds a handle to the neoVI object
int iRetVal;
int iCount;
NeoDevice ndNeoToOpen; //created previously

iRetVal = icsneoOpenNeoDevice(&ndNeoToOpen, &hObject, NULL, 1, 0);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim m_hObject As IntPtr '//handle for device
Dim iResult As Integer '//Holds the results from function call
Dim ndNeoToOpen As NeoDevice '//Struct holding detected hardware information
Dim bNetwork(255) As Byte '//List of hardware IDs
Dim iCount As Integer '//counter

'//File NetworkID array
For iCount = 0 To 255
    bNetwork(iCount) = CByte(iCount)
Next iCount
'//Open the first found device, ndNeoToOpen acquired from FindNeoDevices
iResult = icsneoOpenNeoDevice(ndNeoToOpen(0), m_hObject, bNetwork(0), 1, 0)
If CBool(iResult) Then
    MsgBox("Port Opened OK!")
Else
    MsgBox("Problem Opening Port")
    Exit Sub
End If
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
IntPtr m_hObject; //handle for device
int iResult; //Holds the results from function call
NeoDevice ndNeoToOpen = new NeoDevice(); //Struct holding detected hardware information
byte[] bNetwork = new byte[255]; //List of hardware IDs
int iCount; //counter

//File NetworkID array
for (iCount = 0; iCount < 255; iCount++)
{
    bNetwork[iCount] = Convert.ToByte(iCount);
}
//Open the first found device, ndNeoToOpen acquired from FindNeoDevices
iResult = icsNeoDll.icsneoOpenNeoDevice(ref ndNeoToOpen, ref m_hObject, ref bNetwork[0], 1, 0);
if (iResult == 1)
{
    MessageBox.Show("Port Opened OK!");
}
else
{
    MessageBox.Show("Problem Opening Port");
    return;
}
```
{% endtab %}
{% endtabs %}
