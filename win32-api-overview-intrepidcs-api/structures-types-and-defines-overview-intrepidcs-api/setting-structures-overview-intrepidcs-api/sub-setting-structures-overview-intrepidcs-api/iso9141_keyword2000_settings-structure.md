# ISO9141\_KEYWORD2000\_SETTINGS Structure

**This structure defines settings for ISO9141 and Keyword 2000 networks on neoVI Fire devices.**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef VS_MODIFIER struct
{
    icscm_uint32 Baudrate;
    icscm_uint16 spbrg;
    icscm_uint16 brgh;
    ISO9141_KW2000__INIT_STEP init_steps[16];  //See the ISO9141_KW2000__INIT_STEP structure
    icscm_uint8 init_step_count;
    icscm_uint16 p2_500us;
    icscm_uint16 p3_500us;
    icscm_uint16 p4_500us;
    icscm_uint16 chksum_enabled;
} ISO9141_KEYWORD2000_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)>
Public Structure ISO9141_KEYWORD2000_SETTINGS
    Dim Baudrate As Int32
    Dim spbrg As Int16
    Dim brgh As Int16
    Dim Init_Step_0 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_1 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_2 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_3 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_4 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_5 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_6 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_7 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_8 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_9 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_10 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_11 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_12 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_13 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_14 As ISO9141_KEYWORD2000__INIT_STEP
    Dim Init_Step_15 As ISO9141_KEYWORD2000__INIT_STEP
    Dim init_step_count As Byte
    Dim p2_500us As Int16
    Dim p3_500us As Int16
    Dim p4_500us As Int16
    Dim um_enabled As Int16
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct ISO9141_KEYWORD2000_SETTINGS
{
    public UInt32 Baudrate;
    public UInt16 spbrg;
    public UInt16 brgh;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_0;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_1;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_2;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_3;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_4;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_5;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_6;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_7;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_8;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_9;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_10;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_11;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_12;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_13;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_14;
    public ISO9141_KEYWORD2000__INIT_STEP Init_Step_15;
    public byte init_step_count;
    public UInt16 p2_500us;
    public UInt16 p3_500us;
    public UInt16 p4_500us;
    public UInt16 chksum_enabled;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                                                                              | Description                                                                   |
| ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [icscm\_uint32](../intrepid-api-data-types.md)                                                    | Baudrate Baudrate to use                                                      |
| [icscm\_uint16](../intrepid-api-data-types.md) spbrg                                              | Not used, set to 0                                                            |
| [icscm\_uint16](../intrepid-api-data-types.md) brgh                                               | Not used, set to 0                                                            |
| [ISO9141\_KW2000\_\_INIT\_STEP](iso9141\_keyword2000\_\_init\_step-structure.md) init\_steps\[16] | Init table configuration structure                                            |
| [icscm\_uint8](../intrepid-api-data-types.md) init\_step\_count                                   | Number of steps configured in ISO9141\_KW2000\_\_INIT\_STEP for Init waveform |
| [icscm\_uint16](../intrepid-api-data-types.md) p2\_500us                                          | Rx Inter Message Spacing in 500µs ticks                                       |
| [icscm\_uint16](../intrepid-api-data-types.md) p3\_500us                                          | Tx InterMessage Spacing in 500µs ticks                                        |
| [icscm\_uint16](../intrepid-api-data-types.md) p4\_500us                                          | Tx Inter Byte Spacing in 500µs ticks                                          |
| [icscm\_uint16](../intrepid-api-data-types.md) chksum\_enabled                                    | Option to enable checksum calculation Enable = 1 Disable = 0                  |
