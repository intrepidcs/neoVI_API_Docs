# ValidateHObject Method - intrepidcs API

This method is used to determine if a driver object is valid.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoValidateHObject(void * hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoValidateHObject Lib “icsneo40.dll” (ByVal hObject As IntPtr) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoValidateHObject(IntPtr hObject);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created by [OpenNeoDevice](../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md).

**Return Values**

1 if the hObject is valid. 0 if the object is invalid.

**Remarks**

A driver object will be invalid if it was never initialized by [OpenNeoDevice](../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md). Calling [ClosePort ](../basic-functions-overview-intrepidcs-api/closeport-method-intrepidcs-api.md)will not invalidate a driver object; only [FreeObject](../basic-functions-overview-intrepidcs-api/freeobject-method-intrepidcs-api.md) will do so.

### Examples

{% tabs %}
{% tab title="C/C++ Example:" %}
```cpp
if(Convert::ToBoolean(icsneoValidateHObject(m_hObject)))
{
    cmdCheckHardwareHandle->Text = "Good";
}
else
{
    cmdCheckHardwareHandle->Text = "Lost";
}
```
{% endtab %}

{% tab title="C# Example:" %}
```csharp
if (Convert.ToBoolean (icsNeoDll.icsneoValidateHObject(m_hObject)))
{
    cmdCheckHardwareHandle.Text = "Good";
}
else
{
    cmdCheckHardwareHandle.Text = "Lost";
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example:" %}
```vbnet
If (CBool(icsneoValidateHObject(m_hObject))) Then
    cmdCheckHardwareHandle.Text = "Good"
Else
    cmdCheckHardwareHandle.Text = "Lost"
End If
```
{% endtab %}
{% endtabs %}
