# LOGGER\_SETTINGS Structure

**Structure for logging settings**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint8_t extraction_timeout;
   uint8_t rsvd0;
   uint8_t rsvd1;
   uint8_t rsvd2;
}LOGGER_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure LOGGER_SETTINGS
   Dim extraction_timeout As Byte
   Dim rsvd0 As Byte
   Dim rsvd1 As Byte
   Dim rsvd2 As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct LOGGER_SETTINGS
{
   public byte extraction_timeout;
   public byte rsvd0;
   public byte rsvd1;
   public byte rsvd2;
}
```
{% endtab %}
{% endtabs %}

#### Remarks

| Item                | Description                                                                                                                                                                                                 |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| extraction\_timeout | <p>Not Defined</p><table><thead><tr><th>Bit 7</th><th>Bit 6-0</th></tr></thead><tbody><tr><td>1=disable coremini/logging during extraction for timeout</td><td>Timeout in seconds</td></tr></tbody></table> |
| rsvd0               | Not Defined                                                                                                                                                                                                 |
| rsvd1               | Not Defined                                                                                                                                                                                                 |
| rsvd2               | Not Defined                                                                                                                                                                                                 |
