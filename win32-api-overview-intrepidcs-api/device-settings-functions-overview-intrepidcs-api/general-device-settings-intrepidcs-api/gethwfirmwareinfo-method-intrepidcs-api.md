# GetHWFirmwareInfo Method - intrepidcs API

This method returns the firmware version of the open neoVI device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoGetHWFirmwareInfo(void * hObject, stAPIFirmwareInfo *pInfo);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoGetHWFirmwareInfo Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByRef pInfo As stAPIFirmwareInfo) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoGetHWFirmwareInfo(intPtr hObject, ref stAPIFirmwareInfo pInfo);
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

This method returns the firmware version stored in the open neoVI device.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
stAPIFirmwareInfo FirmwareInfo;
int iResult;

iResult = icsneoGetHWFirmwareInfo(m_hObject, &FirmwareInfo);
if(iResult == 0)
{
    MessageBox::Show("Problem getting the neoVI's firmware information");
    return;
}
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
stAPIFirmwareInfo FirmwareInfo = new stAPIFirmwareInfo();
int iResult;

iResult = icsNeoDll.icsneoGetHWFirmwareInfo(m_hObject, ref FirmwareInfo);
if(iResult == 0)
{
    MessageBox.Show("Problem getting the neoVI's firmware information");
    return;
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim FirmwareInfo As stAPIFirmwareInfo
Dim iResult As Integer

iResult = icsneoGetHWFirmwareInfo(m_hObject, FirmwareInfo)
If iResult = 0 Then
    MsgBox("Problem getting the neoVI's firmware information")
    Exit Sub
End If
```
{% endtab %}
{% endtabs %}
