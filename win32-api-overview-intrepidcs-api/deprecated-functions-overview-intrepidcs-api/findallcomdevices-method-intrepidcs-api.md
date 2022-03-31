# FindAllCOMDevices Method - intrepidcs API

**This function is deprecated. Use** [**FindNeoDevices**](findneodevices-method-intrepidcs-api.md) **instead.**

**This method returns the number of COM (both serial and USB serial) hardware devices connected to the PC.**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoFindAllCOMDevices(int lDriverType,
int lGetSerialNumbers,
int lStopAtFirst,
int lUSBCommOnly,
int *p_lDeviceTypes,
int *p_lComPorts,
int *p_lSerialNumbers,
int *lNumDevices);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoFindAllCOMDevices Lib “icsneo40.dll” _
(ByVal lDriverID As Integer, ByVal lGetSerialNumbers As Integer, _
ByVal lStopAtFirst As Integer, ByVal iUSBCommOnly As Integer, _
ByRef p_lDeviceTypes As Integer, ByRef p_lComPorts As Integer, _
ByRef p_lSerialNumbers As Integer, ByRef lNumDevices As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoFindAllCOMDevices(int lDriverID, int lGetSerialNumbers,int lStopAtFirst, int iUSBCommOnly, ref int p_lDeviceTypes, ref int p_lComPorts,ref int p_lSerialNumber, ref int lNumDevices);
```
{% endtab %}
{% endtabs %}

**Parameters**

lDriverType

\[in] Specifies which neoVI driver to use. This should always be set to INTREPIDCS\_DRIVER\_STANDARD (0).

lGetSerialNumbers

\[in] Specifies whether the serial numbers should be read from the device (iGetSerialNumbers=1). Getting serial numbers will take longer than not doing it therefore so set this to zero if not required for the application. If a device is already opened the serial number cannot be read.

lStopAtFirst

\[in] Indicates whether the function should stop at the first device found (lStopAtFirst=1). This is useful when you only have one device connected to the PC.

lUSBCommOnly

\[in] Indicates to search USB serial devices only (lUSBCommOnly=1). Normal COM ports will not be searched. Normal COM port searches will take longer to execute.

p\_lDeviceTypes

\[out] Pointer to array of at least 255 elements. This array will be filled in with the type of device found. The valid device types include INTREPIDCS\_DEVICE\_NEO4 (0), INTREPIDCS\_DEVICE\_VCAN (1), or INTREPIDCS\_DEVICE\_NEO6 (2).

p\_lComPorts

\[out] Pointer to array of at least 255 elements. This array will be filled in with the com port numbers of each connected device.

p\_lSerialNumbers

\[out] Pointer to array of at least 255 elements. This array will be filled in with the serial number of each device if argument lGetSerialNumbers=1.

iNumDevices

\[out] Points to a value which contains the number of devices found.

**Return Values**

If this function operates successfully the return value will be 1. If the function fails the return value will be zero.

**Remarks**

None.

### Examples

{% tabs %}
{% tab title="C/C++ Example:" %}
```cpp
Opens first device on USB Com port either a ValueCAN or neoVI PRO

int iDeviceTypes[255];
int iComPort[255];
int iSerialNum[255];
int iOpenedStates[255];
int iDeviceNumbers[255];
int iNumDevices;

if (icsneoFindAllCOMDevices(INTREPIDCS_DRIVER_STANDARD, 0,1,1,iDeviceTypes,iComPort,iSerialNum,&iNumDevices))
{

    if (iNumDevices > 0)
    {

        lResult = icsneoOpenPortEx(iComPort[0] ,NEOVI_COMMTYPE_RS232,
                                                                        INTREPIDCS_DRIVER_STANDARD,0,57600,1,bNetworkID, &hObject);

    if (lResult == 0)
        MessageBox(hWnd,TEXT("Problem Opening Port"),TEXT("neoVI Example"),0);
    else
    {

            MessageBox(hWnd,TEXT("Port Opened Successfully"),TEXT("neoVI Example"),0);
        }

    }
}
else
    MessageBox(hWnd,TEXT("Problem Opening Port"),TEXT("neoVI Example"),0);

}
else

    MessageBox(hWnd,TEXT("Problem Opening Port"),TEXT("neoVI Example"),0);
```
{% endtab %}

{% tab title="C# Example:" %}
```csharp
This example demonstrates loading a list box with all the devices connected to the PC

int lResult = 0; //Storage for Result of Function call
int[] iDevices = new int[127]; //Array for the device numbers
int[] iSerialNumbers = new int[127]; //Araay for serial numbers of attached devices
int[] iOpenedStatus = new int[127]; //Array of the status of the driver
int iNumDevices = 0; //Storage for the number of devices
int[] iCommPortNumbers = new int[127]; //Array of Comm Port numbers in use
int Counter = 0; //Counter for Counting things

//Call function for Finding all Comm deivces
lResult = icsNeoDll.icsneoFindAllCOMDevices(Convert.ToInt32 (eDRIVER_TYPE.INTREPIDCS_DRIVER_STANDARD), 1,0,0,ref iDevices[0],ref iCommPortNumbers[0], ref iSerialNumbers[0],ref
iNumDevices)

//Check the status of the funciton call
if(lResult==1)
{
    //Fill in list box with device findings
    for(Counter=0;Counter<127; Counter++)
    {
        lstCommDevices.Items.Add("Device Type-" + Convert.ToString(iDevices[Counter]) + " SN-" + Convert.ToString(iSerialNumbers[Counter]) + " Port #" + Convert.ToString(iCommPortNumbers[Counter]));
    }
}
else
{
    //display error box if could not find anything
    MessageBox.Show("Could Not Find anything");
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example:" %}
```vbnet
This example demonstrates loading a list box with all the devices connected to the PC

Dim lResult As Integer ''Storage for Result of Function call
Dim iDevices(127) As Integer ''Array for the device numbers
Dim iSerialNumbers(127) As Integer ''Array for Serial numbers of attached devices
Dim iOpenedStatus(127) As Integer ''Array of Status of Driver
Dim iNumDevices As Integer ''Storage for the number of devices
Dim iCommPortNumbers(127) As Integer ''Array of Comm port numbers in use
Dim Counter As Integer ''Counter for counting things

''Function call for Finding all of the Comm devices
lResult = icsneoFindAllCOMDevices(INTREPIDCS_DRIVER_STANDARD, 1, 0, 0, iDevices(0), iCommPortNumbers(0), iSerialNumbers(0), iNumDevices)
''check the results
If lResult = 1 Then
    For Counter = 0 To 127
    ''Fill list box with device findings
    lstCommDevices.Items.Add("Device Type-" + Convert.ToString(iDevices(Counter)) + _
        " SN-" + Convert.ToString(iSerialNumbers(Counter)) + " Port #" + Convert.ToString(iCommPortNumbers(Counter)))
Next Counter
Else
    ''Display error message if could not find anything
    MsgBox("Could not find anything")
End If
```
{% endtab %}
{% endtabs %}
