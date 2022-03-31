# GetPerformanceParameters Method - intrepidcs API

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoGetPerformanceParameters(void * hObject, int * iBufferCount, int * iBufferMax, int * iOverFlowCount, int * iReserved1, int * iReserved2,int * iReserved3,int * iReserved4,int * iReserved5)
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoGetPerformanceParameters Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByRef iBufferCount As Integer, ByRef iBufferMax As Integer, ByRef iOverFlowCount As Integer, ByRef iReserved1 As Integer, ByRef iReserved2 As Integer, ByRef iReserved3 As Integer, ByRef iReserved4 As Integer, ByRef iReserved5 As Integer) As Integer
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern int icsneoGetPerformanceParameters(IntPtr hObject,ref int iBufferCount, ref int iBufferMax, ref int iOverFlowCount , ref int iReserved1, ref int iReserved2 , ref int iReserved3, ref int iReserved4 ,ref int iReserved5);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created with the OpenPort method.

iBufferCount

\[out] Specifies the driver object created with the OpenPort method.

IBufferMax

\[out] Specifies the size of the buffer.

iOverFlowCount

\[out] Indicates the the number of overflows that have occurred since the last successful OpenPort method was called.

iReserved1

\[out] Reserved. Set to 0.

iReserved2

\[out] Reserved. Set to 0.

iReserved3

\[out] Reserved. Set to 0.

iReserved4

\[out] Reserved. Set to 0.

iReserved5

\[out] Reserved. Set to 0.

**Return Values**

This function returns the 1 when successful. 0 if otherwise.

**Remarks**

XX.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoGetPerformanceParameters(m_hObject, &iBufferCount, &iBufferMax, &iOverFlowCount, &iReserved1, &iReserved2, &iReserved3, &iReserved4, &iReserved5);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
lResult = icsneoGetPerformanceParameters(m_hObject, iBufferCount, iBufferMax, iOverFlowCount, iReserved1, iReserved2, iReserved3, iReserved4, iReserved5)

If CBool(lResult) Then
    txtBufferCount.Text = iBufferCount
    txtBufferMax.Text = iBufferMax
    txtOverflowCount.Text = iOverFlowCount
End If
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
lResult = icsNeoDll.icsneoGetPerformanceParameters(m_hObject, ref iBufferCount, ref iBufferMax, ref iOverFlowCount, ref iReserved1, ref iReserved2, ref iReserved3, ref iReserved4, ref iReserved5);

if(lResult=1)
{
    txtBufferCount.Text = Convert.ToString(iBufferCount);
    txtBufferMax.Text = Convert.ToString(iBufferMax);
    txtOverflowCount.Text = Convert.ToString(iOverFlowCount);
}
```
{% endtab %}
{% endtabs %}
