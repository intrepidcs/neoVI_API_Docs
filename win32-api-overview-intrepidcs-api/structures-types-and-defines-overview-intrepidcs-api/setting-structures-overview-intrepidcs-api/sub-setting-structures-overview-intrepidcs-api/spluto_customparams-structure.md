# SPluto\_CustomParams Structure

This structure defines a sub structure for SRADPlutoSettings

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   unsigned char mode0;
   unsigned char mode1;
   unsigned char mode2;
   unsigned char mode3;
   unsigned char mode4;
   unsigned char speed0;
   unsigned char speed1;
   unsigned char speed2;
   unsigned char speed3;
   unsigned char speed4;
   unsigned char PhyEnable0;
   unsigned char PhyEnable1;
   unsigned char PhyEnable2;
   unsigned char PhyEnable3;
   unsigned char PhyEnable4;
   unsigned char ae1Select;
   unsigned char usbSelect;
   unsigned char pad;
}SPluto_CustomParams;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SPluto_CustomParams
   Dim mode0 As Byte
   Dim mode1 As Byte
   Dim mode2 As Byte
   Dim mode3 As Byte
   Dim mode4 As Byte
   Dim speed0 As Byte
   Dim speed1 As Byte
   Dim speed2 As Byte
   Dim speed3 As Byte
   Dim speed4 As Byte
   Dim PhyEnable0 As Byte
   Dim PhyEnable1 As Byte
   Dim PhyEnable2 As Byte
   Dim PhyEnable3 As Byte
   Dim PhyEnable4 As Byte
   Dim ae1Select As Byte
   Dim usbSelect As Byte
   Dim pad As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SPluto_CustomParams
{
   public byte mode0;
   public byte mode1;
   public byte mode2;
   public byte mode3;
   public byte mode4;
   public byte speed0;
   public byte speed1;
   public byte speed2;
   public byte speed3;
   public byte speed4;
   public byte PhyEnable0;
   public byte PhyEnable1;
   public byte PhyEnable2;
   public byte PhyEnable3;
   public byte PhyEnable4;
   public byte ae1Select;
   public byte usbSelect;
   public byte pad;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item       | Description                                                                                                                                                                                     |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| mode0      | <p>First inputs connect Mode</p><p>Auto = 0: Master = 1: Slave :1</p>                                                                                                                           |
| mode1      | <p>Second inputs connect Mode</p><p>Auto = 0: Master = 1: Slave :1</p>                                                                                                                          |
| mode2      | <p>Third inputs connect Mode</p><p>Auto = 0: Master = 1: Slave :1</p>                                                                                                                           |
| mode3      | <p>Fourth inputs connect Mode</p><p>Auto = 0: Master = 1: Slave :1</p>                                                                                                                          |
| mode4      | Not used Set to 0                                                                                                                                                                               |
| speed0     | Sets the Speed of the Channel                                                                                                                                                                   |
| speed1     | Not used set to 0                                                                                                                                                                               |
| speed2     | Not used set to 0                                                                                                                                                                               |
| speed3     | Not used set to 0                                                                                                                                                                               |
| speed4     | Not used set to 0                                                                                                                                                                               |
| PhyEnable0 | Enables the first phy                                                                                                                                                                           |
| PhyEnable1 | Enables the second phy                                                                                                                                                                          |
| PhyEnable2 | Enables the Third phy                                                                                                                                                                           |
| PhyEnable3 | Enables the Fourth phy                                                                                                                                                                          |
| PhyEnable4 | Enables the Fifth phy                                                                                                                                                                           |
| ae1Select  | <p>Sets if the First phy is AE or RJ45</p><p>AE=1: RJ45=0</p>                                                                                                                                   |
| usbSelect  | <p>Sets USB Mode</p><p>USB=0: USB to Ethernet: VSpy and Core Mini are not connected to Ethernet.</p><p>CoreMini=1: CM: VSpy and Core Mini can access Ethernet. USB to Ethernet disconnected</p> |
| pad        | Not Available                                                                                                                                                                                   |
