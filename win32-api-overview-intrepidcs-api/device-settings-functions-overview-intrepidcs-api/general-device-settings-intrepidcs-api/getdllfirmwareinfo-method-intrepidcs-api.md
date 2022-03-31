# GetDLLFirmwareInfo Method - intrepidcs API

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoGetDLLFirmwareInfo(void * hObject, stAPIFirmwareInfo *pInfo);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoGetDLLFirmwareInfo Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByRef pInfo As stAPIFirmwareInfo) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoGetDLLFirmwareInfo(IntPtr hObject, ref stAPIFirmwareInfo pInfo);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created by [OpenNeoDevice](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md).

pInfo

\[out] Pointer to an [stAPIFirmwareInfo](../../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/stapifirmwareinfo-structure.md) structure.

**Return Values**

Returns 1 if successful, 0 if an error occurred.

**Remarks**

This method returns the version information for the neoVI firmware stored within the neoVI DLL API. This is the version that will be written to the neoVI device by the [ForceFirmwareUpdate](forcefirmwareupdate-method-intrepidcs-api.md) method.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
stAPIFirmwareInfo FirmwareInfo;
int iResult;

iResult = icsneoGetDLLFirmwareInfo(m_hObject, &FirmwareInfo);
if(iResult == 0)
{
    MessageBox::Show("Problem getting the version of the firmware stored within the DLL API");
    return;
}
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
stAPIFirmwareInfo FirmwareInfo = new stAPIFirmwareInfo();
int iResult;

iResult = icsNeoDll.icsneoGetDLLFirmwareInfo(m_hObject, ref FirmwareInfo);
if(iResult == 0)
{
    MessageBox.Show("Problem getting the version of the firmware stored within the DLL API");
    return;
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim FirmwareInfo As stAPIFirmwareInfo
Dim iResult As Integer

iResult = icsneoGetDLLFirmwareInfo(m_hObject, FirmwareInfo)
If iResult = 0 Then
    MsgBox("Problem getting the version of the firmware stored within the DLL API")
    Exit Sub
End If
```
{% endtab %}
{% endtabs %}
