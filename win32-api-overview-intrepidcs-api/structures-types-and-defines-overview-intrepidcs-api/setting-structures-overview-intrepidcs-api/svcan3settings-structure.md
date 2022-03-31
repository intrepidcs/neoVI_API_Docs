# SVCAN3Settings Structure

This structure defines various settings for the ValueCAN3 device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef VS_MODIFIER struct _SVCAN3Settings
{
    CAN_SETTINGS can1;
    CAN_SETTINGS can2;
    icscm_uint16 network_enables;
    icscm_uint16 network_enabled_on_boot;
    icscm_int16 iso15765_separation_time_offset;
    icscm_uint16 perf_en;
    icscm_uint16 misc_io_initial_ddr;
    icscm_uint16 misc_io_initial_latch;
    icscm_uint16 misc_io_report_period;
    icscm_uint16 misc_io_on_report_events;
} SVCAN3Settings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Structure SVCAN3Settings
    Dim Can1 As CAN_SETTINGS
    Dim Can2 As CAN_SETTINGS
    Dim Network_enables As Int16
    Dim Network_enabled_on_boot As Int16
    Dim Iso15765_separation_time_offset As Int16
    Dim Perf_en As Int16
    Dim Misc_io_initial_ddr As Int16
    Dim Misc_io_initial_latch As Int16
    Dim Misc_io_report_period As Int16
    Dim Misc_io_on_report_events As Int16
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct SVCAN3Settings
{
    public CAN_SETTINGS can1;
    public CAN_SETTINGS can2;
    public UInt16 network_enables;
    public UInt16 network_enabled_on_boot;
    public UInt16 iso15765_separation_time_offset;
    public UInt16 perf_en;
    public UInt16 misc_io_initial_ddr;
    public UInt16 misc_io_initial_latch;
    public UInt16 misc_io_report_period;
    public UInt16 misc_io_on_report_events;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Element**

| Item                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CAN\_SETTINGS can1                              | See [CAN\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/can\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| CAN\_SETTINGS can2                              | See [CAN\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/can\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| icscm\_uint16 network\_enables                  | <p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><p>Bit field values:</p><p>HSCAN1 : 0 MSCAN : 1</p>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| icscm\_uint16 network\_enabled\_on\_boot        | <p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| icscm\_int16 iso15765\_separation\_time\_offset | <p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.</p><p>Default value = 0.</p><p>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.- 998.4 us: iso15765_separation_time_offset = -156</p> |
| icscm\_uint16 perf\_en                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| icscm\_uint16 misc\_io\_initial\_ddr            | <p>MISC IO Initial Data Direction Register. Controls the initial data direction of the tristates on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an input and bit value 1 signifies and output. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0.</p><p>Examples:</p><p>Set MISC1 to be output, all else input: misc_io_initial_ddr = 1</p><p>Set MISC1and MISC2 to be output, all else input: misc_io_initial_ddr = 3 (11 binary)</p><p>Set all MISC pins to output: misc_io_initial_ddr = 65535 (1111111111111111 binary)</p>                                                                                                                                                                                                                                                                     |
| icscm\_uint16 misc\_io\_initial\_latch          | <p>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage (ground) and bit value 1 signifies high voltage (3.3 V). Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0.</p><p>Examples:</p><p>Set MISC1 to be high, all else low: misc_io_initial_latch = 1</p><p>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)</p><p>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)</p><p>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</p>                                                                        |
| icscm\_uint16 misc\_io\_report\_period          | <p>Period in milliseconds of device report message holding digital and analog data.</p><p>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| icscm\_uint16 misc\_io\_on\_report\_events      | <p>Bitfield holding enables for various report triggers for the General IO report.</p><p>Default value = 0.</p><p>Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>REPORT_ON_PERIODIC : 0</td><td>REPORT_ON_LED2 : 8</td></tr><tr><td>REPORT_ON_MISC1 : 1</td><td>REPORT_ON_KLINE : 9</td></tr><tr><td>REPORT_ON_MISC2 : 2</td><td>REPORT_ON_MISC3_AIN : 10</td></tr><tr><td>REPORT_ON_MISC3 : 3</td><td>REPORT_ON_MISC4_AIN : 11</td></tr><tr><td>REPORT_ON_MISC4 : 4</td><td>REPORT_ON_MISC5_AIN : 12</td></tr><tr><td>REPORT_ON_MISC5 : 5</td><td>REPORT_ON_MISC6_AIN : 13</td></tr><tr><td>REPORT_ON_MISC6 : 6</td><td></td></tr><tr><td>REPORT_ON_LED1 : 7</td><td></td></tr></tbody></table>                                                                                                                                                             |
