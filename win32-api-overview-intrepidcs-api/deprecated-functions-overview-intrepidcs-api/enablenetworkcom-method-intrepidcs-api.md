# EnableNetworkCom Method - intrepidcs API

**This function is deprecated. Use the EnableNetworkRXQueue method instead.**

**This method enables or disables all vehicle network rx data.**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoEnableNetworkCom(int hObject,int lEnable);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoEnableNetworkCom Lib “icsneo40.dll” (ByVal hObject As Integer, ByVal lEnable As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoEnableNetworkCom(int hObject, int lEnable);
```
{% endtab %}
{% endtabs %}

**Parameters**

lEnable

\[in] When 1 it will enable network receive. When 0 it will disable network receive.

**Return Values**

This function returns the 1 when successful. 0 if otherwise.

**Remarks**

This function will enable and disable network traffic for all client applications connected to the neoVI. The icsneoEnableNetworkRXQueue function can be used to enable and disable the receive message queue for individual applications.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoEnableNetworkCom(m_hObject,0);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Call icsneoEnableNetworkCom(m_hObject, 0)
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
icsNeoDll.icsneoEnableNetworkCom(m_hObject,0);
```
{% endtab %}
{% endtabs %}
