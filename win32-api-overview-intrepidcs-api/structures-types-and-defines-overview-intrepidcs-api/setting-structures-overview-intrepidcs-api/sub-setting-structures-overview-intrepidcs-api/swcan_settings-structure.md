# SWCAN\_SETTINGS Structure

This structure defines settings for SWCAN networks on neoVI Fire devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef VS_MODIFIER struct
{
    icscm_uint8 Mode;
    icscm_uint8 SetBaudrate;
    icscm_uint8 Baudrate;
    icscm_uint8 NetworkType;
    icscm_uint8 TqSeg1;
    icscm_uint8 TqSeg2;
    icscm_uint8 TqProp;
    icscm_uint8 TqSync;
    icscm_uint16 BRP;
    icscm_uint16 high_speed_auto_switch;
    icscm_uint16 auto_baud;
} SWCAN_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SWCAN_SETTINGS
    Dim Mode As Byte
    Dim SetBaudrate As Byte
    Dim Baudrate As Byte
    Dim NetworkType As Byte
    Dim TqSeg1 As Byte
    Dim TqSeg2 As Byte
    Dim TqProp As Byte
    Dim TqSync As Byte
    Dim BRP As Int16
    Dim high_speed_auto_switch As Int16
    Dim auto_baud As Int16
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SWCAN_SETTINGS
{
    public byte Mode;
    public byte SetBaudrate;
    public byte Baudrate;
    public byte NetworkType;
    public byte TqSeg1;
    public byte TqSeg2;
    public byte TqProp;
    public byte TqSync;
    public UInt16 BRP;
    public UInt16 high_speed_auto_switch;
    public UInt16 auto_baud;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [icscm\_uint8](../intrepid-api-data-types.md) Mode                       | <p>CAN controller mode when the neoVI device goes online or runs a CoreMini script.</p><p>Default value = 0</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>NORMAL</td><td>0</td></tr><tr><td>DISABLED</td><td>1</td></tr><tr><td>LISTEN ONLY</td><td>3</td></tr><tr><td>LISTEN ALL</td><td>7</td></tr></tbody></table>                                                                                                                                                                                                                                                                                                                                                                                              |
| [icscm\_uint8](../intrepid-api-data-types.md) SetBaudrate                | <p>The bit rate of a CAN channel can be selected one of two ways. It can either be selected from a list of common bit rates (SetBaudrate=1) or the user can specify the CAN timing parameters (SetBaudrate=0)</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>AUTO (Select from bitrate list using Baudrate parameter)</td><td>0</td></tr><tr><td>USE_TQ (Use time quanta parameters</td><td>1</td></tr></tbody></table>                                                                                                                                                                                                                                                                                             |
| [icscm\_uint8](../intrepid-api-data-types.md) Baudrate                   | <p>The bit rate of a CAN channel can be selected from a list of common bit rates Write the correct enumeration for the desired bit rate and ensure that SetBaudrate is 1(auto)</p><p>Default value = 8</p><p>Note: This parameter is only applicable if SetBaudrate = 1 20000</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>0</td><td></td></tr><tr><td>33333</td><td>1</td></tr><tr><td>50000</td><td>2</td></tr><tr><td>62500</td><td>3</td></tr><tr><td>83333</td><td>4</td></tr><tr><td>100000</td><td>5</td></tr><tr><td>125000</td><td>6</td></tr><tr><td>250000</td><td>7</td></tr><tr><td>500000</td><td>8</td></tr><tr><td>800000</td><td>9</td></tr><tr><td>1000000</td><td>10</td></tr></tbody></table> |
| [icscm\_uint8](../intrepid-api-data-types.md) NetworkType                | Currently Not used. Will be supoprted in neoVI Yellow to software select which CAN transceiver to use (DW vs SW vs LSFT).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [icscm\_uint8](../intrepid-api-data-types.md) TqSeg1                     | Phase 1 segment                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [icscm\_uint8](../intrepid-api-data-types.md) TqSeg2                     | Phase 2 segment                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [icscm\_uint8](../intrepid-api-data-types.md) TqProp                     | Propagation delay                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [icscm\_uint8](../intrepid-api-data-types.md) TqSync                     | Syncro jump width                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [icscm\_uint16](../intrepid-api-data-types.md) BRP                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [icscm\_uint16](../intrepid-api-data-types.md) high\_speed\_auto\_switch | <p></p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>DISABLED</td><td>0</td></tr><tr><td>NO_RESISTOR</td><td>1</td></tr><tr><td>WITH_RESISTOR</td><td>2</td></tr></tbody></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [icscm\_uint16](../intrepid-api-data-types.md) auto\_baud                | <p>Enables the auto bitrate feature. 1 = enable, 0 = disable.</p><p>Default value = 0</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
