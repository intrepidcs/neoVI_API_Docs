# ForceFirmwareUpdate Method - intrepidcs API

This method forces the firmware on neoVI device to be updated.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
void _stdcall icsneoForceFirmwareUpdate(void * hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoForceFirmwareUpdate Lib “icsneo40.dll” (ByVal hObject As IntPtr)
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern void icsneoForceFirmwareUpdate(IntPtr hObject);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created by [OpenNeoDevice](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md).

**Return Values**

None.

**Remarks**

This method is used to force the firmware on a neoVI device to be updated to the version stored in the DLL API.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoForceFirmwareUpdate(hObject);
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
icsNeoDll.icsneoForceFirmwareUpdate(m_hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Call icsneoForceFirmwareUpdate(m_hObject)
```
{% endtab %}
{% endtabs %}
