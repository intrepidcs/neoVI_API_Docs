# ISO15765\_EnableNetworks Method - intrepidcs API

This method enables the use of ISO15765-2 on a CAN network. icsneoISO15765\_EnableNetwroks must be called before using icsneoISO15765\_TransmitMessage or icsneoISO15765\_ReceiveMessage.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
void _stdcall icsneoISO15765_EnableNetworks(void * hObject, unsigned int iNetwork);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoISO15765_EnableNetworks Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByVal Network As UInt32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)]
public static extern Int32 icsneoISO15765_EnableNetworks (IntPtr hObject, UInt32 Network);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle which specifies the driver object created with the OpenPort method.

lNetwork

\[in] Specifies which CAN network the status is requested for. Can be one of the following values:

| Network  | Value |
| -------- | ----- |
| HS CAN   | 1     |
| MS CAN   | 2     |
| HS CAN 2 | 4     |
| HS CAN 3 | 8     |
| SW CAN   | 16    |
| HS CAN 4 | 20    |
| HS CAN 5 | 24    |
| HS CAN 6 | 28    |
| HS CAN 7 | 32    |
| SW CAN 2 | 36    |

**Return Values**

None.

**Remarks**

None.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
lResult = icsneoISO15765_EnableNetworks(m_hObject,NETID_HSCAN);
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
lResult = icsNeoDll.icsneoISO15765_EnableNetworks(m_hObject,(int)eNETWORK_ID.NETID_HSCAN);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
lResult = icsneoISO15765_EnableNetworks(m_hObject, NETID_HSCAN)
```
{% endtab %}
{% endtabs %}
