# ETHERNET\_SETTINGS Structure

This structure defines various settings for Ethernet networks.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
    unsigned char duplex;
    unsigned char link_speed;
    unsigned char auto_neg;
    unsigned char led_mode;
    unsigned char rsvd0;
    unsigned char rsvd1;
    unsigned char rsvd2;
    unsigned char rsvd3;
}ETHERNET_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure ETHERNET_SETTINGS
    Dim duplex As Byte
    Dim link_speed As Byte
    Dim auto_neg As Byte
    Dim led_mode As Byte
    Dim rsvd0 As Byte
    Dim rsvd1 As Byte
    Dim rsvd2 As Byte
    Dim rsvd3 As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct ETHERNET_SETTINGS
{
    public byte duplex;
    public byte link_speed;
    public byte auto_neg;
    public byte led_mode;
    public byte rsvd0;
    public byte rsvd1;
    public byte rsvd2;
    public byte rsvd3;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item        | Description                                                                          |
| ----------- | ------------------------------------------------------------------------------------ |
| duplex      | <p>Sets the Duplex mode.</p><p>0=Half 1=Full</p>                                     |
| link\_speed | <p>Sets the speed for the network</p><p>0=10Mbps 1=100Mbps</p>                       |
| auto\_neg   | <p>Enables Auto-Negotiate</p><p>0=Disabled 1=Enabled</p>                             |
| led\_mode   | <p>Sets the function of the Ethernet IDs</p><p>0=link 1=activity 2=link/activity</p> |
| rsvd0       | Reserved Set to 0                                                                    |
| rsvd1       | Reserved Set to 0                                                                    |
| rsvd2       | Reserved Set to 0                                                                    |
| rsvd3       | Reserved Set to 0                                                                    |
