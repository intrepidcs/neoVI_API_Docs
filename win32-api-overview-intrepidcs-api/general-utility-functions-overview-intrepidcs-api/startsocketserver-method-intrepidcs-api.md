# StartSocketServer Method - intrepidcs API

This method starts the TCP/IP socket server at a specified port.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoStartSockServer(int hObject, int iPort);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoStartSockServer Lib “icsneo40.dll” (ByVal hObject As Integer, ByVal iPort As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoStartSockServer(int hObject, int iPort);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle which specifies the driver object created by [OpenNeoDevice](../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md)

iPort

\[in] specifies the TCP/IP Port where the server will be established.

**Return Values**

If the server was started successfully the return value will be non-zero.

**Remarks**

This method creates a TCP/IP server in the DLL. This server can be attached to by any TCP/IP clients using the RAW API or using the DLL by specifying TCP/IP with [OpenNeoDevice](../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md). Only one server is allowed at a time.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoStartSockServer(hObject, iPort);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
bStatus = icsneoStartSockServer(m_hObject, iPort)) '// start the socket server
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
iStatus = icsNeoDll.icsneoStartSockServer(m_hObject, Convert.ToInt32(txtServerPort.Text));
```
{% endtab %}
{% endtabs %}
