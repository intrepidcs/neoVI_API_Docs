---
cover: ../../.gitbook/assets/new-cover-image.png
coverY: 0
---

# FindDevices Method

This method returns the neoVI hardware devices connected to the PC.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoFindDevices(NeoDeviceEx* pNeoDeviceEx, int* pNumDevices ,unsigned int* DeviceTypes,unsigned int numDeviceTypes,POptionsFindNeoEx* pOptionsNeoEx,unsigned int* reserved); 
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoFindDevices Lib "icsneo40.dll" (ByRef pNeoDevice As NeoDeviceEx, ByRef pNumDevices As Int32, ByRef DeviceTypes As UInt32, ByVal numDeviceTypes As UInt32, ByRef pOptionsFindNeoEx As OptionsNeoEx, ByVal reserved As UInt32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport("icsneo40.dll")]
public static extern Int32 icsneoFindDevices(ref NeoDeviceEx pNeoDevice, ref Int32 pNumDevices, UInt32 DeviceTypes, UInt32 numDeviceTypes, ref OptionsNeoEx pOptionsNeoEx, UInt32 reserved);
```
{% endtab %}
{% endtabs %}

**Parameters**

_pNeoDeviceEx_\
\[out] This is the address of the first element of an array of [NeoDeviceEx](../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/neodeviceex-structure.md) structure. This array can be as big as 255 devices. You must specify the size of the pNeoDeviceEx array in the pNumDevices parameter. The number of devices found will be limited to the value of pNumberofDevices or 255, whichever is lower. Each returned NeoDevice structure will contain information for each device such as its type, device ‘handle’ and serial number.

_pNumberOfDevices_\
\[in/out] In: Specifies the size of the pNeoDevices array. Must be in the range 0 to 255.\
Out: Specifies the number of neo devices that were found. This can be in the range 0 to 255.\
\
_DeviceTypes_\
\_\_ \[in] This is an array of device types to look for. Specifies the types of neoVI devices to find. Each element in the array need to have a value for the device type to look for. Currently supported values are:

NEODEVICE\_UNKNOWN = 0x00000000

NEODEVICE\_BLUE = 0x00000001

NEODEVICE\_ECU\_AVB = 0x00000002

NEODEVICE\_RADSUPERMOON = 0x00000003

NEODEVICE\_DW\_VCAN = 0x00000004

NEODEVICE\_RADMOON2 = 0x00000005

NEODEVICE\_RADGIGALOG = 0x00000006

NEODEVICE\_VCAN41 = 0x00000007

NEODEVICE\_FIRE = 0x00000008

NEODEVICE\_RADPLUTO = 0x00000009

NEODEVICE\_VCAN42\_EL = 0x0000000a

NEODEVICE\_RADIO\_CANHUB = 0x0000000b

NEODEVICE\_NEOECU12 = 0x0000000c

NEODEVICE\_OBD2\_LCBADGE = 0x0000000d

NEODEVICE\_RAD\_MOON\_DUO = 0x0000000e

NEODEVICE\_VCAN3 = 0x00000010

NEODEVICE\_RADJUPITER = 0x00000011

NEODEVICE\_VCAN4\_IND = 0x00000012

NEODEVICE\_GIGASTAR = 0x00000013

NEODEVICE\_ECU22 = 0x00000015

NEODEVICE\_RED = 0x00000040

NEODEVICE\_ECU = 0x00000080

NEODEVICE\_IEVB = 0x00000100

NEODEVICE\_PENDANT = 0x00000200

NEODEVICE\_OBD2\_PRO = 0x00000400

NEODEVICE\_PLASMA = 0x00001000

NEODEVICE\_NEOANALOG = 0x00004000

NEODEVICE\_CT\_OBD = 0x00008000

NEODEVICE\_ION = 0x00040000

NEODEVICE\_RADSTAR = 0x00080000

NEODEVICE\_VCAN44 = 0x00200000

NEODEVICE\_VCAN42 = 0x00400000

NEODEVICE\_CMPROBE = 0x00800000

NEODEVICE\_EEVB = 0x01000000

NEODEVICE\_VCANRF = 0x02000000

NEODEVICE\_FIRE2 = 0x04000000

NEODEVICE\_FLEX = 0x08000000

NEODEVICE\_RADGALAXY = 0x10000000

NEODEVICE\_RADSTAR2 = 0x20000000

NEODEVICE\_VIVIDCAN = 0x40000000

NEODEVICE\_OBD2\_SIM = 0x80000000

NEODEVICE\_ALL = = 0xFFFFBFFF

Constants are defined in appropriate header or module. pNumDevicTypes

\[in] In: Specifies the size of the DeviceTypes array. Must be in the range 0 to 255.

_pOptionsNeoEx_

\[in] CAN netowork ID for connecting to devices over CAN. Set to null for USB or Ethernet connections.

**Return Values**

1 if the function succeeded. 0 if it failed for any reason. If the function succeeds but no devices are found 1 will still be returned and pNumberOfDevices will equal 0.

**Remarks**

The NeoDevice array elements that are returned with this function may be passed to [OpenNeoDevice ](openneodevice-method-intrepidcs-api.md)so that individual neoVI devices can be opened.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
NeoDeviceEx Devices[255];
unsigned long lDevTypes;
int iNumDevices = 255;
int iRetVal = 0;
int lDevTypes;

lDevTypes = NEODEVICE_ALL;

iRetVal = icsneoFindDevices(Devices, &iNumberOfDevices,NULL,0,NULL,0);
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
int iResult;//Holds the results from function call
NeoDeviceEx ndNeoToOpen = new NeoDeviceEx(); ; //Struct holding detected hardware information
int iNumberOfDevices; //Number of hardware devices to look for
int lDevTypes; //Holds the device types to look for
lDevTypes = NEODEVICE_ALL;

//Set the number of devices to find
iNumberOfDevices = 1;
//Search for connected hardware
iResult = icsNeoDll.icsneoFindDevices(ref ndNeoToOpenex[0],ref iNumberOfDevices, 0, 0,ref neoDeviceOption, 0);
if (iResult == 0)
{
    MessageBox.Show("Problem finding devices");
    return;
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example:" %}
```vbnet
Dim iResult As Integer '//Holds the results from function call
Dim ndNeoToOpenex As NeoDeviceEx '//Struct holding detected hardware information
Dim iNumberOfDevices As Integer '//Number of hardware devices to look for
Dim lDevTypes As Integer '//Holds the device types to look for
Dim neoDeviceOption As OptionsNeoEx = New OptionsNeoEx '//Not using CAN 0 out


'//Set the devices to look for
lDevTypes = NEODEVICE_ALL
'//Set the number of devices to find
iNumberOfDevices = 1
'//Search for connected hardware
iResult = icsneoFindDevices(ndNeoToOpenex(0), iNumberOfDevices, 0, 0, neoDeviceOption, 0)
If (iResult = 0) Then MsgBox("Problem finding devices")
```
{% endtab %}
{% endtabs %}
