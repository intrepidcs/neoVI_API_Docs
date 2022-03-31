# icsSpyTime Structure

Structure for GetRTC and SetRTC

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct
{
  unsigned char sec;
  unsigned char min;
  unsigned char hour;
  unsigned char day;
  unsigned char month;
  unsigned char year;
}icsSpyTime;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=8)> Public Structure icsSpyTime
  Dim sec As Byte
  Dim min As Byte
  Dim hour As Byte
  Dim day As Byte
  Dim month As Byte
  Dim year As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=8)]
public struct icsSpyTime
{
  public byte sec;
  public byte min;
  public byte hour;
  public byte day;
  public byte month;
  public byte year;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item  | Description                  |
| ----- | ---------------------------- |
| sec   | Seconds place to read or set |
| min   | Minutes place to read or set |
| hour  | Hours place to read or set   |
| day   | Day place to read or set     |
| month | Month place to read or set   |
| year  | Year Place to read or set    |
