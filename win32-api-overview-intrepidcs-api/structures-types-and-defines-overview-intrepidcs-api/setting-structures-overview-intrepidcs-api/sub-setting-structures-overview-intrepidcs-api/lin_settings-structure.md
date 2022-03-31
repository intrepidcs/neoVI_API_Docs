# LIN\_SETTINGS Structure

This structure defines settings for LIN networks on supported hardware devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
 {
  unsigned int Baudrate;
  unsigned short spbrg;
  unsigned char brgh;
  unsigned char NumBitsDelay;
  unsigned char MasterResistor;
  unsigned char Mode;
 }LIN_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure LIN_SETTINGS
    Dim Baudrate As UInt32
    Dim spbrg As UInt16
    Dim brgh As Byte
    Dim NumBitsDelay As Byte
    Dim MasterResistor As Byte
    Dim Mode As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct LIN_SETTINGS
{
    public UInt32 Baudrate;
    public UInt16 spbrg;
    public byte brgh;
    public byte NumBitsDelay;
    public byte MasterResistor;
    public byte Mode;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item           | Description                                              |
| -------------- | -------------------------------------------------------- |
| Baudrate       | Baudrate to be set                                       |
| spbrg          | Only use with neoVI FIRE. 40Mhz/Baudrate/16-1 = spbrg    |
| brgh           | Set to 0                                                 |
| NumBitsDelay   | Delay to set between Header and Slave data. Default is 0 |
| MasterResistor | Enable for Master Resistor Off=0: On=1:                  |
| Mode           | Sets the LIN Mode Sleep=0: Slow=1: Normal=2: Fast=2:     |
