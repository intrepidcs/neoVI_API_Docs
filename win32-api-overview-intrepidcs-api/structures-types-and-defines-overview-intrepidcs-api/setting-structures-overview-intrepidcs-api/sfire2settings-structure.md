# SFire2Settings Structure

This structure defines various settings for the neoVI FIRE2 device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint16_t perf_en;
   CAN_SETTINGS can1;
   CANFD_SETTINGS canfd1;
   CAN_SETTINGS can2;
   CANFD_SETTINGS canfd2;
   CAN_SETTINGS can3;
   CANFD_SETTINGS canfd3;
   CAN_SETTINGS can4;
   CANFD_SETTINGS canfd4;
   CAN_SETTINGS can5;
   CANFD_SETTINGS canfd5;
   CAN_SETTINGS can6;
   CANFD_SETTINGS canfd6;
   CAN_SETTINGS can7;
   CANFD_SETTINGS canfd7;
   CAN_SETTINGS can8;
   CANFD_SETTINGS canfd8;
   SWCAN_SETTINGS swcan1;
   uint16_t network_enables;
   SWCAN_SETTINGS swcan2;
   uint16_t network_enables_2;
   CAN_SETTINGS lsftcan1;
   CAN_SETTINGS lsftcan2;
   LIN_SETTINGS lin1;
   uint16_t misc_io_initial_ddr;
   LIN_SETTINGS lin2;
   uint16_t misc_io_initial_latch;
   LIN_SETTINGS lin3;
   uint16_t misc_io_report_period;
   LIN_SETTINGS lin4;
   uint16_t misc_io_on_report_events;
   LIN_SETTINGS lin5;
   uint16_t misc_io_analog_enable;
   uint16_t ain_sample_period;
   uint16_t ain_threshold;
   uint32_t pwr_man_timeout;
   uint16_t pwr_man_enable;
   uint16_t network_enabled_on_boot;
   uint16_t iso15765_separation_time_offset;
   uint16_t iso_9141_kwp_enable_reserved;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_1;
   uint16_t iso_parity_1;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_2;
   uint16_t iso_parity_2;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_3;
   uint16_t iso_parity_3;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_4;
   uint16_t iso_parity_4;
   uint16_t iso_msg_termination_1;
   uint16_t iso_msg_termination_2;
   uint16_t iso_msg_termination_3;
   uint16_t iso_msg_termination_4;
   uint16_t idle_wakeup_network_enables_1;
   uint16_t idle_wakeup_network_enables_2;
   uint16_t network_enables_3;
   uint16_t idle_wakeup_network_enables_3;
   uint16_t can_switch_mode;
   STextAPISettings text_api;
   uint64_t termination_enables;
   LIN_SETTINGS lin6;
   ETHERNET_SETTINGS ethernet;
   uint16_t slaveVnetA;
   uint16_t slaveVnetB;
   uint32_t flags;
   uint16_t digitalIoThresholdTicks;
   uint16_t digitalIoThresholdEnable;
}SFire2Settings; 
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SFire2Settings
   Dim perf_en As UInt16
   Dim can1 As CAN_SETTINGS
   Dim canfd1 As CANFD_SETTINGS
   Dim can2 As CAN_SETTINGS
   Dim canfd2 As CANFD_SETTINGS
   Dim can3 As CAN_SETTINGS
   Dim canfd3 As CANFD_SETTINGS
   Dim can4 As CAN_SETTINGS
   Dim canfd4 As CANFD_SETTINGS
   Dim can5 As CAN_SETTINGS
   Dim canfd5 As CANFD_SETTINGS
   Dim can6 As CAN_SETTINGS
   Dim canfd6 As CANFD_SETTINGS
   Dim can7 As CAN_SETTINGS
   Dim canfd7 As CANFD_SETTINGS
   Dim can8 As CAN_SETTINGS
   Dim canfd8 As CANFD_SETTINGS
   Dim swcan1 As SWCAN_SETTINGS
   Dim network_enables As UInt16
   Dim swcan2 As SWCAN_SETTINGS
   Dim network_enables_2 As UInt16
   Dim lsftcan1 As CAN_SETTINGS
   Dim lsftcan2 As CAN_SETTINGS
   Dim lin1 As LIN_SETTINGS
   Dim misc_io_initial_ddr As UInt16
   Dim lin2 As LIN_SETTINGS
   Dim misc_io_initial_latch As UInt16
   Dim lin3 As LIN_SETTINGS
   Dim misc_io_report_period As UInt16
   Dim lin4 As LIN_SETTINGS
   Dim misc_io_on_report_events As UInt16
   Dim lin5 As LIN_SETTINGS
   Dim misc_io_analog_enable As UInt16
   Dim ain_sample_period As UInt16
   Dim ain_threshold As UInt16
   Dim pwr_man_timeout As UInt32
   Dim pwr_man_enable As UInt16
   Dim network_enabled_on_boot As UInt16
   Dim iso15765_separation_time_offset As UInt16
   Dim iso_9141_kwp_enable_reserved As UInt16
   Dim iso9141_kwp_settings_1 As ISO9141_KEYWORD2000_SETTINGS
   Dim iso_parity_1 As UInt16
   Dim iso9141_kwp_settings_2 As ISO9141_KEYWORD2000_SETTINGS
   Dim iso_parity_2 As UInt16
   Dim iso9141_kwp_settings_3 As ISO9141_KEYWORD2000_SETTINGS
   Dim iso_parity_3 As UInt16
   Dim iso9141_kwp_settings_4 As ISO9141_KEYWORD2000_SETTINGS
   Dim iso_parity_4 As UInt16
   Dim iso_msg_termination_1 As UInt16
   Dim iso_msg_termination_2 As UInt16
   Dim iso_msg_termination_3 As UInt16
   Dim iso_msg_termination_4 As UInt16
   Dim idle_wakeup_network_enables_1 As UInt16
   Dim idle_wakeup_network_enables_2 As UInt16
   Dim network_enables_3 As UInt16
   Dim idle_wakeup_network_enables_3 As UInt16
   Dim can_switch_mode As UInt16
   Dim text_api As STextAPISettings
   Dim termination_enables As UInt64
   Dim lin6 As LIN_SETTINGS
   Dim ethernet As ETHERNET_SETTINGS
   Dim slaveVnetA As UInt16
   Dim slaveVnetB As UInt16
   Dim flags As UInt32
   Dim digitalIoThresholdTicks As UInt16
   Dim digitalIoThresholdEnable As UInt16
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SFire2Settings
{
   public UInt16 perf_en;
   public CAN_SETTINGS can1;
   public CANFD_SETTINGS canfd1;
   public CAN_SETTINGS can2;
   public CANFD_SETTINGS canfd2;
   public CAN_SETTINGS can3;
   public CANFD_SETTINGS canfd3;
   public CAN_SETTINGS can4;
   public CANFD_SETTINGS canfd4;
   public CAN_SETTINGS can5;
   public CANFD_SETTINGS canfd5;
   public CAN_SETTINGS can6;
   public CANFD_SETTINGS canfd6;
   public CAN_SETTINGS can7;
   public CANFD_SETTINGS canfd7;
   public CAN_SETTINGS can8;
   public CANFD_SETTINGS canfd8;
   public SWCAN_SETTINGS swcan1;
   public UInt16 network_enables;
   public SWCAN_SETTINGS swcan2;
   public UInt16 network_enables_2;
   public CAN_SETTINGS lsftcan1;
   public CAN_SETTINGS lsftcan2;
   public LIN_SETTINGS lin1;
   public UInt16 misc_io_initial_ddr;
   public LIN_SETTINGS lin2;
   public UInt16 misc_io_initial_latch;
   public LIN_SETTINGS lin3;
   public UInt16 misc_io_report_period;
   public LIN_SETTINGS lin4;
   public UInt16 misc_io_on_report_events;
   public LIN_SETTINGS lin5;
   public UInt16 misc_io_analog_enable;
   public UInt16 ain_sample_period;
   public UInt16 ain_threshold;
   public UInt32 pwr_man_timeout;
   public UInt16 pwr_man_enable;
   public UInt16 network_enabled_on_boot;
   public UInt16 iso15765_separation_time_offset;
   public UInt16 iso_9141_kwp_enable_reserved;
   public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_1;
   public UInt16 iso_parity_1;
   public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_2;
   public UInt16 iso_parity_2;
   public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_3;
   public UInt16 iso_parity_3;
   public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_4;
   public UInt16 iso_parity_4;
   public UInt16 iso_msg_termination_1;
   public UInt16 iso_msg_termination_2;
   public UInt16 iso_msg_termination_3;
   public UInt16 iso_msg_termination_4;
   public UInt16 idle_wakeup_network_enables_1;
   public UInt16 idle_wakeup_network_enables_2;
   public UInt16 network_enables_3;
   public UInt16 idle_wakeup_network_enables_3;
   public UInt16 can_switch_mode;
   public STextAPISettings text_api;
   public UInt64 termination_enables;
   public LIN_SETTINGS lin6;
   public ETHERNET_SETTINGS ethernet;
   public UInt16 slaveVnetA;
   public UInt16 slaveVnetB;
   public UInt32 flags;
   public UInt16 digitalIoThresholdTicks;
   public UInt16 digitalIoThresholdEnable;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

<table><thead><tr><th width="334">Item</th><th>Description</th></tr></thead><tbody><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can7</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd7</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can8</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd8</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>swcan1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>NA : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>NA : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>swcan2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> structure</td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>lsftcan1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>lsftcan2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_initial_ddr</td><td>MISC IO Initial Data Direction Register. Controls the initial data direction of the tri-states on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an input and bit value 1 signifies and output. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.<br><br>Default value = 0<br><br>Examples:<br><br>Set MISC1 to be output, all else input: misc_io_initial_ddr = 1<br><br>Set MISC1and MISC2 to be output, all else input: misc_io_initial_ddr = 3 (11 binary)<br><br>Set all MISC pins to output: misc_io_initial_ddr = 65535 (1111111111111111 binary)</td></tr><tr><td>lin2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_initial_latch</td><td>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage and bit value 1 signifies high voltage. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.<br><br>Default value = 0<br><br>Examples:<br><br>Set MISC1 to be high, all else low: misc_io_initial_latch = 1<br><br>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)<br><br>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)<br><br>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</td></tr><tr><td>lin3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_report_period</td><td>Period in milliseconds of device report message holding digital and analog data.<br><br>Default value = 100<br><br>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</td></tr><tr><td>lin4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_on_report_events</td><td><p>Bitfield holding enables for various report triggers for the General IO report. Default value = 0 Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>REPORT_ON_PERIODIC : 0</td><td>REPORT_ON_MISC1 : 1</td></tr><tr><td>REPORT_ON_MISC2 : 2</td><td>REPORT_ON_MISC3 : 3</td></tr><tr><td>REPORT_ON_MISC4 : 4</td><td>REPORT_ON_MISC5 : 5</td></tr><tr><td>REPORT_ON_MISC6 : 6</td><td>REPORT_ON_LED1 : 7</td></tr><tr><td>REPORT_ON_LED2 : 8</td><td>REPORT_ON_KLINE : 9</td></tr><tr><td>REPORT_ON_MISC3_AIN : 10</td><td>REPORT_ON_MISC4_AIN : 11</td></tr><tr><td>REPORT_ON_MISC5_AIN : 12</td><td>REPORT_ON_MISC6_AIN : 13</td></tr></tbody></table></td></tr><tr><td>lin5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_analog_enable</td><td>MISC IO Analog Enable Register. Controls the initial analog enables on all misc analog pins. Each bit corresponds to an individual misc pin that supports analog input. Bit value of 0 signifies that corresponding misc pin is digital only, and bit value 1 signifies corresponding misc pin is analog. Note that because some MISC pins are not capable of analog they are not included in the register. For example neoVI FIRE's analog pins are MISC3-MISC6, therefore bit 0 corresponds to MISC3's analog enable. Bit values corresponding to non existent pins have no effect.<br><br>Default value = 0<br><br>Examples:<br><br>Set MISC3 to be analog, all else digital. (neoVI FIRE) : misc_io_analog_enable = 1<br><br>Set MISC3 and MISC4 to be analog, all else digital. (neoVI FIRE): misc_io_analog_enable = 3 (11 binary)<br><br>Set all MISC pins to high: misc_io_analog_enable = 65535 (1111111111111111 binary)<br>Note: that in order for analog inputs to work correctly the corresponding bit in misc_io_analog_enable must be set to 1.</td></tr><tr><td>ain_sample_period</td><td>Controls how long the Analog to Digital Converter samples before preforming a convert in milliseconds. If it is set to zero the hardware will perform the conversion immediately after sampling. This option defaults to 0 but is accessible so that high impedance analog sources can still be used by manually increasing the sample period.<br><br>Default value = 0</td></tr><tr><td>ain_threshold</td><td>Percent of full voltage change required to trigger a REPORT_ON_MISCX_AIN event. Valid range is 0-100.<br><br>Default value = 0<br><br>Examples:<br><br>Report fires every time ADC value changes: ain_threshold = 0<br><br>Report fires every time ADC value changes by 400 mV: ain_threshold = 1<br><br>Report fires every time ADC value changes by 800 mV: ain_threshold = 2<br><br>Report fires every time ADC value changes by 40 V (Unpractical): ain_threshold = 100<br><br>Note: Periodic reporting requires proper misc_io_on_report_events bit to be set.</td></tr><tr><td>pwr_man_timeout</td><td>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.<br><br>Default value = 10000</td></tr><tr><td>pwr_man_enable</td><td>1 = enable Power Management, 0 = disable.<br><br>Default value = 0</td></tr><tr><td>network_enabled_on_boot</td><td>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.<br><br>Default value = 0</td></tr><tr><td>iso15765_separation_time_offset</td><td>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.<br><br>Default value = 0<br><br>Examples:<br><br>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0<br><br>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156<br><br>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.- 998.4 us:<br>iso15765_separation_time_offset = -156</td></tr><tr><td>iso_9141_kwp_enable_reserved</td><td>Reserved</td></tr><tr><td>iso9141_kwp_settings_1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_1</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso9141_kwp_settings_2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_2</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso9141_kwp_settings_3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_3</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso9141_kwp_settings_4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_4</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination_1</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td>iso_msg_termination_2</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td>iso_msg_termination_3</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td>iso_msg_termination_4</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td>idle_wakeup_network_enables_1</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>NA : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>NA : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_2</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_3</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>NA : 11</td></tr><tr><td>NA : 12</td><td>NA : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_3</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>NA : 11</td></tr><tr><td>NA : 12</td><td>NA : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>can_switch_mode</td><td>Not Available</td></tr><tr><td>text_api</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> structure</td></tr><tr><td>termination_enables</td><td><p>Bitfield containing the termination enables. For the neoVI Fire 2, the termination is grouped into banks. Only 2 form a single bank can be neabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN (Bank0): 0</td><td>MSCAN (Bank1): 1</td><td>HSCAN2 (BANK1) : 5</td></tr><tr><td>HSCAN3 (Bank0) : 8</td><td>HSCAN4 (Bank1): 14</td><td>HSCAN5 (Bank0) : 15</td></tr><tr><td>HSCAN6 (Bank1) : 32</td><td>HSCAN7 (Bank0): 33</td><td></td></tr></tbody></table></td></tr><tr><td>lin6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>ethernet</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure.md">ETHERNET_SETTINGS</a> structure</td></tr><tr><td>slaveVnetA</td><td>Sets the type of VNET is in slot A for ION and Plasma devices<br>eNoVnet = 0<br>eAinVnet = 1<br>eFlexRayVnet = 2<br>eSlaveFireVnet =3<br>eSlaveFireVnetEP = 4<br>eSlaveFire2Vnet = 5<br>eSlaveFire2VnetZ = 6<br>eSlaveMost150 = 7</td></tr><tr><td>slaveVnetB</td><td>Sets the type of VNET is in slot B for Plasma devices<br>eNoVnet = 0<br>eAinVnet = 1<br>eFlexRayVnet = 2<br>eSlaveFireVnet =3<br>eSlaveFireVnetEP = 4<br>eSlaveFire2Vnet = 5<br>eSlaveFire2VnetZ = 6<br>eSlaveMost150 = 7</td></tr><tr><td>flags</td><td>Bitfield with misc settings for the device. List below gives the parameter with the bit number to have set to enable.<br><br>Disable USB Check On Boot : 0<br>Bus Messages To Android (ION and Plasma) : 2</td></tr><tr><td>digitalIoThresholdTicks</td><td>Ticks needed to trigger digital change</td></tr><tr><td>digitalIoThresholdEnable</td><td>Enable digital change thresholding</td></tr><tr><td>timeSync</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/timesync_icshardware_settings-structure.md">TIMESYNC_ICSHARDWARE_SETTINGS</a> structure</td></tr><tr><td>disk</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/disk_settings-structure.md">DISK_SETTINGS</a> structure</td></tr><tr><td>ethernet2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings2-structure.md">ETHERNET_SETTINGS2</a> structure</td></tr></tbody></table>
