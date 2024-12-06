# SFireSettings Structure

This structure defines various settings for the neoVI Fire device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef VS_MODIFIER struct _SFireSettings
{ 
    CAN_SETTINGS can1;   
    CAN_SETTINGS can2;
    CAN_SETTINGS can3;
    CAN_SETTINGS can4;
    SWCAN_SETTINGS swcan;    
    CAN_SETTINGS lsftcan;
    LIN_SETTINGS lin1;      
    LIN_SETTINGS lin2;
    LIN_SETTINGS lin3;
    LIN_SETTINGS lin4;
    icscm_uint16 cgi_enable_reserved;
    icscm_uint16 cgi_baud;
    icscm_uint16 cgi_tx_ifs_bit_times;
    icscm_uint16 cgi_rx_ifs_bit_times;
    icscm_uint16 cgi_chksum_enable;
    icscm_uint16 network_enables;
    icscm_uint16 network_enabled_on_boot;
    icscm_uint16 pwm_man_timeout;
    icscm_uint16 pwr_man_enable;
    icscm_uint16 misc_io_initial_ddr;
    icscm_uint16 misc_io_initial_latch;
    icscm_uint16 misc_io_analog_enable;
    icscm_uint16 misc_io_report_period;
    icscm_uint16 misc_io_on_report_events;
    icscm_uint16 ain_sample_period;
    icscm_uint16 ain_threshold;
    icscm_uint16 iso15765_separation_time_offset;
    icscm_uint16 iso9141_kwp_enable_reserved;
    ISO9141_KW2000SETTINGS iso9141_kwp_settings;
    icscm_uint16 perf_en;
    icscm_uint16 iso_parity;
    icscm_uint16 iso_msg_termination;
    icscm_uint16 iso_tester_pullup_enable;
    icscm_uint16 network_enables_2;
    ISO9141_KW2000SETTINGS iso9141_kwp_settings2;
    icscm_uint16 iso_parity_2; 
    icscm_uint16 iso_msg_termination_2;
     ISO9141_KW2000SETTINGS iso9141_kwp_settings_3;
    icscm_uint16 iso_parity_3; 
    icscm_uint16 iso_msg_termination_3; 
    ISO9141_KW2000SETTINGS iso9141_kwp_settings_4;
    icscm_uint16 iso_parity_4; 
    icscm_uint16 iso_msg_termination_4; 
    icscm_uint16 fast_init_network_enables_1;
    icscm_uint16 fast_init_network_enables_2;
    UART_SETTINGS uart;
    UART_SETTINGS uart2;
    STextAPISettings text_api;
}SFireSettings; 
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SFireSettings
    Dim can1 As CAN_SETTINGS
    Dim can2 As CAN_SETTINGS
    Dim can3 As CAN_SETTINGS
    Dim can4 As CAN_SETTINGS
    Dim swcan As SWCAN_SETTINGS 
    Dim lsftcan As CAN_SETTINGS
    Dim lin1 As LIN_SETTINGS
    Dim lin2 As LIN_SETTINGS
    Dim lin3 As LIN_SETTINGS
    Dim lin4 As LIN_SETTINGS
    Dim cgi_enable_reserved As UInt16
    Dim cgi_baud As UInt16
    Dim cgi_tx_ifs_bit_times As UInt16
    Dim cgi_rx_ifs_bit_times As UInt16
    Dim cgi_chksum_enable As UInt16
    Dim network_enables As UInt16
    Dim network_enabled_on_boot As UInt16
    Dim pwm_man_timeout As UInt16
    Dim pwr_man_enable As UInt16
    Dim misc_io_initial_ddr As UInt16
    Dim misc_io_initial_latch As UInt16
    Dim misc_io_analog_enable As UInt16
    Dim misc_io_report_period As UInt16
    Dim misc_io_on_report_events As UInt16
    Dim ain_sample_period As UInt16
    Dim ain_threshold As UInt16
    Dim iso15765_separation_time_offset As UInt16
    Dim iso9141_kwp_enable_reserved As UInt16
    iso9141_kwp_settings As ISO9141_KEYWORD2000_SETTINGS
    Dim perf_en As UInt16
    Dim iso_parity As UInt16
    Dim iso_msg_termination As UInt16
    Dim iso_tester_pullup_enable As UInt16
    Dim network_enables_2 As UInt16
    Dim iso9141_kwp_settings2 As ISO9141_KEYWORD2000_SETTINGS
    Dim iso_parity_2 As UInt16
    Dim iso_msg_termination_2 As UInt16
    Dim iso9141_kwp_settings_3 As ISO9141_KEYWORD2000_SETTINGS
    Dim iso_parity_3 As UInt16
    Dim iso_msg_termination_3 As UInt16
    Dim iso9141_kwp_settings_4 As ISO9141_KEYWORD2000_SETTINGS
    Dim iso_parity_4 As UInt16
    Dim iso_msg_termination_4 As UInt16
    Dim fast_init_network_enables_1 As UInt16
    Dim fast_init_network_enables_2 As UInt16
    Dim uart As UART_SETTINGS
    Dim uart2 As UART_SETTINGS
    Dim text_api As STextAPISettings
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SFireSettings
{
    public CAN_SETTINGS can1;
    public CAN_SETTINGS can2; 
    public CAN_SETTINGS can3;
    public CAN_SETTINGS can4;
    public SWCAN_SETTINGS swcan;
    public CAN_SETTINGS lsftcan;
    public LIN_SETTINGS lin1;
    public LIN_SETTINGS lin2;
    public LIN_SETTINGS lin3;
    public LIN_SETTINGS lin4;
    public UInt16 cgi_enable_reserved;
    public UInt16 cgi_baud;
    public UInt16 cgi_tx_ifs_bit_times;
    public UInt16 cgi_rx_ifs_bit_times;
    public UInt16 cgi_chksum_enable;
    public UInt16 network_enables;
    public UInt16 network_enabled_on_boot;
    public UInt16 pwm_man_timeout;
    public UInt16 pwr_man_enable;
    public UInt16 misc_io_initial_ddr;
    public UInt16 misc_io_initial_latch;
    public UInt16 misc_io_analog_enable;
    public UInt16 misc_io_report_period;
    public UInt16 misc_io_on_report_events;
    public UInt16 ain_sample_period;
    public UInt16 ain_threshold;
    public UInt16 iso15765_separation_time_offset;
    public UInt16 iso9141_kwp_enable_reserved;
    public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
    public UInt16 perf_en;
    public UInt16 iso_parity;
    public UInt16 iso_msg_termination;
    public UInt16 iso_tester_pullup_enable;
    public UInt16 network_enables_2;
    public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings2;
    public UInt16 iso_parity_2;
    public UInt16 iso_msg_termination_2;
    public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings3;
    public UInt16 iso_parity_3;
    public UInt16 iso_msg_termination_3;
    public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_4;
    public UInt16 iso_parity_4;
    public UInt16 iso_msg_termination_4; 
    public UInt16 fast_init_network_enables_1;
    public UInt16 fast_init_network_enables_2;
    public UART_SETTINGS uart;
    public UART_SETTINGS uart2;
    public STextAPISettings text_api;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

#### Structure Elements

<table><thead><tr><th width="437">Item</th><th>Description</th></tr></thead><tbody><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> can3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> can4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> swcan</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> lsftcan</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTING</a> lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTING</a> lin2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTING</a> lin3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTING</a> lin4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> cgi_enable_reserved</td><td><em><strong>Deprecated. Enable and disable CGI using the network_enables element.</strong></em></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> cgi_baud</td><td>CGI network baud rate:<br>625 = 625,000kb<br>115 = 115,200kb</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> cgi_tx_ifs_bit_times</td><td>CGI network - Number of bits separating transmit frames. neoVI will ensure this number of idle bit times in between successive transmitted frames. Valid values (1-65535).<br><br><em><strong>Default value = 13</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> cgi_rx_ifs_bit_times</td><td>CGI network - Number of bits separating received frames. neoVI identifies the end of a rx frame when there is no CGI bus activity for this given number of bit times. Valid values (1-65535).<br><br><em><strong>Default value = 13</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> cgi_chksum_enable</td><td>If enabled neoVI will append a 16 bit checksum to all transmitted frames. 1 to enable, 0 to disable.<br><br><em><strong>Default value = 1</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br><br>Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HSCAN1 : 0</td><td>HSCAN3 : 8</td></tr><tr><td>MSCAN : 1</td><td>CGI : 9</td></tr><tr><td>LIN1 : 2</td><td>NA : 10</td></tr><tr><td>LIN2 : 3</td><td>LIN3 : 11</td></tr><tr><td>reserved : 4</td><td>LIN4 : 12</td></tr><tr><td>HSCAN2 : 5</td><td>NA : 13</td></tr><tr><td>LSFT : 6</td><td>NA : 14</td></tr><tr><td>SW_CAN : 7</td><td>NA : 15</td></tr></tbody></table><p>Examples:<br><br>Enable HSCAN1 and HSCAN2: network_enables = 33 (21 hex) (0000000000100001 binary)<br><br>Enable all networks: network_enables = 65535 (FFFF hex) (1111111111111111 binary)<br></p></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> network_enabled_on_boot</td><td>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.<br><br><em><strong>Default value = 0</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> pwm_man_timeout</td><td>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.<br><br><em><strong>Default value = 10000</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> pwr_man_enable</td><td>1 = enable Power Management, 0 = disable.<br><br><em><strong>Default value = 0</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> misc_io_initial_ddr</td><td>MISC IO Initial Data Direction Register. Controls the initial data direction of the tri-states on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an input and bit value 1 signifies and output. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.<br><br><em><strong>Default value = 0</strong></em><br><br>Examples:<br><br>Set MISC1 to be output, all else input: misc_io_initial_ddr = 1<br><br>Set MISC1and MISC2 to be output, all else input: misc_io_initial_ddr = 3 (11 binary)<br><br>Set all MISC pins to output: misc_io_initial_ddr = 65535 (1111111111111111 binary)</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> misc_io_initial_latch</td><td>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage (ground) and bit value 1 signifies high voltage (3.3 V). Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.<br><br><em><strong>Default value = 0</strong></em><br><br>Examples:<br><br>Set MISC1 to be high, all else low: misc_io_initial_latch = 1<br><br>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)<br><br>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)<br><br><em><strong>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</strong></em></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> misc_io_analog_enable</td><td><p>MISC IO Analog Enable Register. Controls the initial analog enables on all misc analog pins. Each bit corresponds to an individual misc pin that supports analog input. Bit value of 0 signifies that corresponding misc pin is digital only, and bit value 1 signifies corresponding misc pin is analog. Note that because some MISC pins are not capable of analog they are not included in the register. For example neoVI FIRE's analog pins are MISC3-MISC6, therefore bit 0 corresponds to MISC3's analog enable. Bit values corresponding to non existent pins have no effect.<br><br><em><strong>Default value = 0</strong></em><br><br>Examples:<br><br>Set MISC3 to be analog, all else digital. (neoVI FIRE) : misc_io_analog_enable = 1<br><br>Set MISC3 and MISC4 to be analog, all else digital. (neoVI FIRE): misc_io_analog_enable = 3 (11 binary)<br><br>Set all MISC pins to high: misc_io_analog_enable = 65535 (1111111111111111 binary)</p><p><em><strong>Note: that in order for analog inputs to work correctly the corresponding bit in misc_io_analog_enable must be set to 1.</strong></em><br></p></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> misc_io_report_period</td><td>Period in milliseconds of device report message holding digital and analog data.<br><br><em><strong>Default value = 100</strong></em><br><br><em><strong>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</strong></em></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> misc_io_on_report_events</td><td><p>Bitfield holding enables for various report triggers for the General IO report.<br><br><em><strong>Default value = 0</strong></em><br><br>Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>REPORT_ON_PERIODIC : 0</td><td>REPORT_ON_LED2 : 8</td></tr><tr><td>REPORT_ON_MISC1 : 1</td><td>REPORT_ON_KLINE : 9</td></tr><tr><td>REPORT_ON_MISC2 : 2</td><td>REPORT_ON_MISC3_AIN : 10</td></tr><tr><td>REPORT_ON_MISC3 : 3</td><td>REPORT_ON_MISC4_AIN : 11</td></tr><tr><td>REPORT_ON_MISC4 : 4</td><td>REPORT_ON_MISC5_AIN : 12</td></tr><tr><td>REPORT_ON_MISC5 : 5</td><td>REPORT_ON_MISC6_AIN : 13</td></tr><tr><td>REPORT_ON_MISC6 : 6</td><td></td></tr><tr><td>REPORT_ON_LED1 : 7</td><td></td></tr></tbody></table></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> ain_sample_period</td><td>Controls how long the Analog to Digital Converter samples before preforming a convert in milliseconds. If it is set to zero the hardware will perform the conversion immediately after sampling. This option defaults to 0 but is accessible so that high impedance analog sources can still be used by manually increasing the sample period.<br><br><em><strong>Default value = 0</strong></em><br></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> ain_threshold</td><td>Percent of full voltage change required to trigger a REPORT_ON_MISCX_AIN event. Valid range is 0-100.<br><br><em><strong>Default value = 0</strong></em><br><br>Examples:<br><br>Report fires every time ADC value changes: ain_threshold = 0<br><br>Report fires every time ADC value changes by 33 mV: ain_threshold = 1<br><br>Report fires every time ADC value changes by 66 mV: ain_threshold = 2<br><br>Report fires every time ADC value changes by 3.3 V (Unpractical): ain_threshold = 100<br><br><em><strong>Note: Periodic reporting requires proper misc_io_on_report_events bit to be set.</strong></em></td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso15765_separation_time_offset</td><td>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.<br><br><em><strong>Default value = 0</strong></em><br><br>Examples:<br><br>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0<br><br>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156<br><br>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.- 998.4 us:<br>iso15765_separation_time_offset = -156</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br><br>Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>Reserved : 4</td></tr><tr><td>KLINE2 : 1</td><td>Reserved : 5</td></tr><tr><td>KLIN3 : 2</td><td>Reserved : 6</td></tr><tr><td>LIN2 : 3</td><td></td></tr></tbody></table></td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> iso9141_kwp_settings</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> structure</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_parity;</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_msg_termination;</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_tester_pullup_enable;</td><td>enables the 510 ohm pull-up resistor on K Line</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> network_enables_2;</td><td></td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> iso9141_kwp_settings2;</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> structure</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_parity_2;</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_msg_termination_2;</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> iso9141_kwp_settings_3;</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> structure</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_parity_3;</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_msg_termination_3;</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> iso9141_kwp_settings_4;</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KW2000SETTINGS</a> structure</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_parity_4;</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> iso_msg_termination_4;</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td><a href="intrepid-api-data-types.md">icscm_uint16</a> fast_init_network_enables;</td><td><p>Bitfield containing the channels to fast wakeup on. Currently only HS and MS CAN are supported</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HSCAN1 : 0</td><td>MSCAN : 1</td></tr></tbody></table><p>Power management must be enabled for this feature to work.</p></td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/uart_settings-structure.md">UART_SETTINGS</a> UART;</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/uart_settings-structure.md">UART_SETTINGS</a> structure</td></tr><tr><td><a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> Text_API;</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> structure</td></tr></tbody></table>
