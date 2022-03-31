# StopSocketServer Method - intrepidcs API

This method starts the TCP/IP socket server at a specified port.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoStopSockServer(int hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoStopSockServer Lib “icsneo40.dll” (ByVal hObject As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoStopSockServer(int hObject);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle to the driver object created by [OpenNeoDevice](../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md)

**Return Values**

If the server has been stopped successfully the return value will be 1. If the function fails the return value will be zero.

**Remarks**

This method should be called when the server created with [StartSocketServer](startsocketserver-method-intrepidcs-api.md).

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoStopSockServer(hObject);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
bStatus = icsneoStopSockServer(m_hObject) '// stop the socket server
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
iStatus = icsNeoDll.icsneoStopSockServer(m_hObject); // stop the socket server
```
{% endtab %}
{% endtabs %}
