---
cover: ../../.gitbook/assets/new-cover-image.png
coverY: 0
---

# FreeObject Method - IntrepidCS API

This method releases system resources used by the neoVI device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
void _stdcall icsneoFreeObject(void * hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoFreeObject Lib “icsneo40.dll” (ByVal hObject As IntPtr)
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern void icsneoFreeObject(IntPtr hObject);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\*\*\*\* \[in] Specifies the driver object created by [OpenNeoDevice](openneodevice-method-intrepidcs-api.md).

**Return Values**

None.

**Remarks**

This method is used to release any resources that were allocated by [OpenNeoDevice](openneodevice-method-intrepidcs-api.md). Applications that create neoVI handles should release them using this method, however, the intrepidCS API will release any resources that it created for the client application when the client application ends and the API is unloaded. The LabVIEW neoClosePort.vi will call the FreeObject API.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoFreeObject(hObject);  //Free the memory associated with our driver object
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
icsNeoDll.icsneoFreeObject(m_hObject); //Free the memory associated with our driver object
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Call icsneoFreeObject(m_hObject)   '//Free the memory associated with our driver object
```
{% endtab %}
{% endtabs %}
