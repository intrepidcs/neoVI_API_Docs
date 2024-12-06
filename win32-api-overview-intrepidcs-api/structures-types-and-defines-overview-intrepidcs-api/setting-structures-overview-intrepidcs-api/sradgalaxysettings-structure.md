# SRADGalaxySettings Structure

Structure defining the parameter in SRADGalaxySettings

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   unsigned short perf_en;
   OP_ETH_GENERAL_SETTINGS opEthGen;
   OP_ETH_SETTINGS opEth1;
   OP_ETH_SETTINGS opEth2;
   OP_ETH_SETTINGS opEth3;
   OP_ETH_SETTINGS opEth4;
   OP_ETH_SETTINGS opEth5;
   OP_ETH_SETTINGS opEth6;
   OP_ETH_SETTINGS opEth7;
   OP_ETH_SETTINGS opEth8;
   OP_ETH_SETTINGS opEth9;
   OP_ETH_SETTINGS opEth10;
   OP_ETH_SETTINGS opEth11;
   OP_ETH_SETTINGS opEth12;
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
   unsigned short network_enables;
   SWCAN_SETTINGS swcan2;
   unsigned short network_enables_2;
   LIN_SETTINGS lin1;
   unsigned short misc_io_initial_ddr;
   unsigned short misc_io_initial_latch;
   unsigned short misc_io_report_period;
   unsigned short misc_io_on_report_events;
   unsigned short misc_io_analog_enable;
   unsigned short ain_sample_period;
   unsigned short ain_threshold;
   unsigned int pwr_man_timeout;
   unsigned short pwr_man_enable;
   unsigned short network_enabled_on_boot;
   unsigned short iso15765_separation_time_offset;
   unsigned short iso_9141_kwp_enable_reserved;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_1;
   unsigned short iso_parity_1;
   unsigned short iso_msg_termination_1;
   unsigned short idle_wakeup_network_enables_1;
   unsigned short idle_wakeup_network_enables_2;
   unsigned short network_enables_3;
   unsigned short idle_wakeup_network_enables_3;
   unsigned short can_switch_mode;
   STextAPISettings text_api;
   TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
   unsigned short hwComLatencyTestEn;
   RAD_REPORTING_SETTINGS reporting;
   DISK_SETTINGS disk;
   LOGGER_SETTINGS logger;
   ETHERNET_SETTINGS2 ethernet1;
   ETHERNET_SETTINGS2 ethernet2;
   int16_t network_enables_4;
   RAD_GPTP_SETTINGS gPTP;
}SRADGalaxySettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SRADGalaxySettings
   Dim perf_en As UInt16
   Dim opEthGen As OP_ETH_GENERAL_SETTINGS
   Dim opEth1 As OP_ETH_SETTINGS
   Dim opEth2 As OP_ETH_SETTINGS
   Dim opEth3 As OP_ETH_SETTINGS
   Dim opEth4 As OP_ETH_SETTINGS
   Dim opEth5 As OP_ETH_SETTINGS
   Dim opEth6 As OP_ETH_SETTINGS
   Dim opEth7 As OP_ETH_SETTINGS
   Dim opEth8 As OP_ETH_SETTINGS
   Dim opEth9 As OP_ETH_SETTINGS
   Dim opEth10 As OP_ETH_SETTINGS
   Dim opEth11 As OP_ETH_SETTINGS
   Dim opEth12 As OP_ETH_SETTINGS
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
   Dim lin1 As LIN_SETTINGS
   Dim misc_io_initial_ddr As UInt16
   Dim misc_io_initial_latch As UInt16
   Dim misc_io_report_period As UInt16
   Dim misc_io_on_report_events As UInt16
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
   Dim iso_msg_termination_1 As UInt16
   Dim idle_wakeup_network_enables_1 As UInt16
   Dim idle_wakeup_network_enables_2 As UInt16
   Dim network_enables_3 As UInt16
   Dim idle_wakeup_network_enables_3 As UInt16
   Dim can_switch_mode As UInt16
   Dim text_api As STextAPISettings
   Dim timeSyncSettings As TIMESYNC_ICSHARDWARE_SETTINGS
   Dim hwComLatencyTestEn As UInt16
   Dim reporting As RAD_REPORTING_SETTINGS
   Dim disk As DISK_SETTINGS
   Dim logger As LOGGER_SETTINGS
   Dim ethernet1 As ETHERNET_SETTINGS2
   Dim ethernet2 As ETHERNET_SETTINGS2
   Dim network_enables_4 As Int16
   Dim gPTP As RAD_GPTP_SETTINGS
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SRADGalaxySettings
{
   public UInt16 perf_en;
   public OP_ETH_GENERAL_SETTINGS opEthGen;
   public OP_ETH_SETTINGS opEth1;
   public OP_ETH_SETTINGS opEth2;
   public OP_ETH_SETTINGS opEth3;
   public OP_ETH_SETTINGS opEth4;
   public OP_ETH_SETTINGS opEth5;
   public OP_ETH_SETTINGS opEth6;
   public OP_ETH_SETTINGS opEth7;
   public OP_ETH_SETTINGS opEth8;
   public OP_ETH_SETTINGS opEth9;
   public OP_ETH_SETTINGS opEth10;
   public OP_ETH_SETTINGS opEth11;
   public OP_ETH_SETTINGS opEth12;
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
   public LIN_SETTINGS lin1;
   public UInt16 misc_io_initial_ddr;
   public UInt16 misc_io_initial_latch;
   public UInt16 misc_io_report_period;
   public UInt16 misc_io_on_report_events;
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
   public UInt16 iso_msg_termination_1;
   public UInt16 idle_wakeup_network_enables_1;
   public UInt16 idle_wakeup_network_enables_2;
   public UInt16 network_enables_3;
   public UInt16 idle_wakeup_network_enables_3;
   public UInt16 can_switch_mode;
   public STextAPISettings text_api;
   public TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
   public UInt16 hwComLatencyTestEn;
   public RAD_REPORTING_SETTINGS reporting;
   public DISK_SETTINGS disk;
   public LOGGER_SETTINGS logger;
   public ETHERNET_SETTINGS2 ethernet1;
   public ETHERNET_SETTINGS2 ethernet2;
   public Int16 network_enables_4;
   public RAD_GPTP_SETTINGS gPTP;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

<table><thead><tr><th width="404">Item</th><th>Description</th></tr></thead><tbody><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>opEthGen</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_general_settings-structure.md">OP_ETH_GENERAL_SETTINGS</a> structure</td></tr><tr><td>opEth1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth7</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth8</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth9</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth10</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth11</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth12</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/op_eth_settings-structure.md">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd5</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd6</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can7</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd7</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can8</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd8</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>swcan1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>swcan2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/swcan_settings-structure.md">SWCAN_SETTINGS</a> structure</td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART: 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_initial_ddr</td><td><p>MISC IO Initial Data Direction Register. Controls the initial data direction of the tri-states on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an input and bit value 1 signifies and output. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC1 to be output, all else input: misc_io_initial_ddr = 1</p><p>Set MISC1and MISC2 to be output, all else input: misc_io_initial_ddr = 3 (11 binary)</p><p>Set all MISC pins to output: misc_io_initial_ddr = 65535 (1111111111111111 binary)</p></td></tr><tr><td>misc_io_initial_latch</td><td><p>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage and bit value 1 signifies high voltage. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC1 to be high, all else low: misc_io_initial_latch = 1</p><p>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)</p><p>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)</p><p>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</p></td></tr><tr><td>misc_io_report_period</td><td><p>Period in milliseconds of device report message holding digital and analog data.</p><p>Default value = 100</p><p>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</p></td></tr><tr><td>misc_io_on_report_events</td><td><p>Bitfield holding enables for various report triggers for the General IO report. Default value = 0 Bit field values:</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>REPORT_ON_PERIODIC : 0</td><td>REPORT_ON_MISC1 : 1</td></tr><tr><td>REPORT_ON_MISC2 : 2</td><td>REPORT_ON_MISC3 : 3</td></tr><tr><td>REPORT_ON_MISC4 : 4</td><td>REPORT_ON_MISC5 : 5</td></tr><tr><td>REPORT_ON_MISC6 : 6</td><td>REPORT_ON_LED1 : 7</td></tr><tr><td>REPORT_ON_LED2 : 8</td><td>REPORT_ON_KLINE : 9</td></tr><tr><td>REPORT_ON_MISC3_AIN : 10</td><td>REPORT_ON_MISC4_AIN : 11</td></tr><tr><td>REPORT_ON_MISC5_AIN : 12</td><td>REPORT_ON_MISC6_AIN : 13</td></tr></tbody></table></td></tr><tr><td>misc_io_analog_enable</td><td><p>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage and bit value 1 signifies high voltage. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC1 to be high, all else low: misc_io_initial_latch = 1</p><p>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)</p><p>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)</p><p>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</p></td></tr><tr><td>ain_sample_period</td><td><p>Controls how long the Analog to Digital Converter samples before preforming a convert in milliseconds. If it is set to zero the hardware will perform the conversion immediately after sampling. This option defaults to 0 but is accessible so that high impedance analog sources can still be used by manually increasing the sample period.</p><p>Default value = 0</p></td></tr><tr><td>ain_threshold</td><td><p>Percent of full voltage change required to trigger a REPORT_ON_MISCX_AIN event. Valid range is 0-100.</p><p>Default value = 0</p><p>Examples:</p><p>Report fires every time ADC value changes: ain_threshold = 0</p><p>Report fires every time ADC value changes by 400 mV: ain_threshold = 1</p><p>Report fires every time ADC value changes by 800 mV: ain_threshold = 2</p><p>Report fires every time ADC value changes by 40 V (Unpractical): ain_threshold = 100</p><p>Note: Periodic reporting requires proper misc_io_on_report_events bit to be set.</p></td></tr><tr><td>pwr_man_timeout</td><td><p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p></td></tr><tr><td>pwr_man_enable</td><td><p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p></td></tr><tr><td>network_enabled_on_boot</td><td><p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0</p></td></tr><tr><td>iso15765_separation_time_offset</td><td><p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.</p><p>Default value = 0</p><p>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.- 998.4 us: iso15765_separation_time_offset = -156</p></td></tr><tr><td>iso_9141_kwp_enable_reserved</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso9141_kwp_settings_1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_1</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination_1</td><td>Not Available</td></tr><tr><td>idle_wakeup_network_enables_1</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_2</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART: 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_3</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>OP_ETH1: 4</td><td>OP_ETH2 : 5</td></tr><tr><td>OP_ETH3 : 6</td><td>OP_ETH4 : 7</td><td>OP_ETH5 : 8</td></tr><tr><td>OP_ETH6 : 9</td><td>OP_ETH7 : 10</td><td>OP_ETH8 : 11</td></tr><tr><td>OP_ETH9 : 12</td><td>OP_ETH10 : 13</td><td>OP_ETH11: 14</td></tr><tr><td>OP_ETH12: 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_3</td><td>Not Available</td></tr><tr><td>can_switch_mode</td><td>Not Available</td></tr><tr><td>text_api</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> structure</td></tr><tr><td>timeSyncSettings</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/timesync_icshardware_settings-structure.md">TIMESYNC_ICSHARDWARE_SETTINGS</a> structure</td></tr><tr><td>hwComLatencyTestEn</td><td>Not Available</td></tr><tr><td>reporting</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/rad_reporting_settings-structure.md">RAD_REPORTING_SETTINGS</a> structure</td></tr><tr><td>disk</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/disk_settings-structure.md">DISK_SETTINGS</a> structure</td></tr><tr><td>logger</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/logger_settings-structure.md">LOGGER_SETTINGS</a> structure</td></tr><tr><td>ethernet1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings2-structure.md">ETHERNET_SETTINGS2</a> structure</td></tr><tr><td>ethernet2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings2-structure.md">ETHERNET_SETTINGS2</a> structure</td></tr><tr><td>network_enables_4</td><td>Not Available</td></tr><tr><td>gPTP</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/rad_gptp_settings-structure.md">RAD_GPTP_SETTINGS</a> structure</td></tr></tbody></table>
