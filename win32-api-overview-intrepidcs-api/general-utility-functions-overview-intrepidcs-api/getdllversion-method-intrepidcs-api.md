# GetDLLVersion Method - intrepidcs API

This method returns the software version of the DLL.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoGetDLLVersion();
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoGetDLLVersion Lib “icsneo40.dll” () As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoGetDLLVersion();
```
{% endtab %}
{% endtabs %}

**Parameters**

None.

**Return Values**

This function returns the version number of the API.

**Remarks**

None.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
char szOut[200];

// get the DLL version and report it
wsprintf(szOut,TEXT("intrepidcs API DLL Version %d\n"), icsneoGetDLLVersion());
MessageBox(hWnd,szOut,TEXT("Message"),MB_ICONINFORMATION);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
'// get the DLL version information and place in Button text
Button1.Text = "Version " + Convert.ToString(icsneoGetDLLVersion)
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
'// get the DLL version information and place in Button text
Button1.Text = "Version " + Convert.ToString(icsNeoDll.icsneoGetDLLVersion());
```
{% endtab %}
{% endtabs %}
