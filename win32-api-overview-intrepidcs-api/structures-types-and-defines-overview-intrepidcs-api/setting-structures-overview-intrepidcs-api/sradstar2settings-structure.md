# SRADStar2Settings Structure

**Structure defining the parameters in SRADStar2Settings**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint16_t perf_en;
   OP_ETH_GENERAL_SETTINGS opEthGen;
   OP_ETH_SETTINGS opEth1;
   OP_ETH_SETTINGS opEth2;
   CAN_SETTINGS can1;
   CANFD_SETTINGS canfd1;
   CAN_SETTINGS can2;
   CANFD_SETTINGS canfd2;
   uint16_t network_enables;
   uint16_t network_enables_2;
   LIN_SETTINGS lin1;
   uint16_t misc_io_initial_ddr;
   uint16_t misc_io_initial_latch;
   uint16_t misc_io_report_period;
   uint16_t misc_io_on_report_events;
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
   uint16_t iso_msg_termination_1;
   uint16_t idle_wakeup_network_enables_1;
   uint16_t idle_wakeup_network_enables_2;
   uint16_t network_enables_3;
   uint16_t idle_wakeup_network_enables_3;
   uint16_t can_switch_mode;
   STextAPISettings text_api;
   uint16_t pc_com_mode;
   TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
   unsigned short hwComLatencyTestEn;
   RAD_REPORTING_SETTINGS reporting;
   ETHERNET_SETTINGS2 ethernet;
   RAD_GPTP_SETTINGS gPTP;
}SRADStar2Settings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SRADStar2Settings
   Dim perf_en As UInt16
   Dim opEthGen As OP_ETH_GENERAL_SETTINGS
   Dim opEth1 As OP_ETH_SETTINGS
   Dim opEth2 As OP_ETH_SETTINGS
   Dim can1 As CAN_SETTINGS
   Dim canfd1 As CANFD_SETTINGS
   Dim can2 As CAN_SETTINGS
   Dim canfd2 As CANFD_SETTINGS
   Dim network_enables As UInt16
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
   Dim pc_com_mode As UInt16
   Dim timeSyncSettings As TIMESYNC_ICSHARDWARE_SETTINGS
   Dim hwComLatencyTestEn As UInt16
   Dim reporting As RAD_REPORTING_SETTINGS
   Dim ethernet As ETHERNET_SETTINGS2
   Dim gPTP As RAD_GPTP_SETTINGS
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SRADStar2Settings
{
   public UInt16 perf_en;
   public OP_ETH_GENERAL_SETTINGS opEthGen;
   public OP_ETH_SETTINGS opEth1;
   public OP_ETH_SETTINGS opEth2;
   public CAN_SETTINGS can1;
   public CANFD_SETTINGS canfd1;
   public CAN_SETTINGS can2;
   public CANFD_SETTINGS canfd2;
   public UInt16 network_enables;
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
   public UInt16 pc_com_mode;
   public TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
   public UInt16 hwComLatencyTestEn;
   public RAD_REPORTING_SETTINGS reporting;
   public ETHERNET_SETTINGS2 ethernet;
   public RAD_GPTP_SETTINGS gPTP;
}
```
{% endtab %}
{% endtabs %}

#### Remarks

<table><thead><tr><th width="444">Item</th><th>Description</th></tr></thead><tbody><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>opEthGen</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/op_eth_general_settings-structure">OP_ETH_GENERAL_SETTINGS</a> structure</td></tr><tr><td>opEth1</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>opEth2</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure">OP_ETH_SETTINGS</a> structure</td></tr><tr><td>can1</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/can_settings-structure">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd1</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/can_settings-structure">CAN_SETTING</a>S structure</td></tr><tr><td>canfd2</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure">CANFD_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br></p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>misc_io_initial_ddr</td><td>Not Used</td></tr><tr><td>misc_io_initial_latch</td><td>Not Used</td></tr><tr><td>misc_io_report_period</td><td>Not Used</td></tr><tr><td>misc_io_on_report_events</td><td>Not Used</td></tr><tr><td>misc_io_analog_enable</td><td>Not Used</td></tr><tr><td>ain_sample_period</td><td>Not Used</td></tr><tr><td>ain_threshold</td><td>Not Used</td></tr><tr><td>pwr_man_timeout</td><td>Not Used</td></tr><tr><td>pwr_man_enable</td><td>Not Used</td></tr><tr><td>network_enabled_on_boot</td><td><p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.<br></p><p>Default value = 0</p></td></tr><tr><td>iso15765_separation_time_offset</td><td><p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.<br></p><p>Default value = 0<br></p><p>Examples:<br></p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0<br></p><p>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156<br></p><p>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.- 998.4 us:<br>iso15765_separation_time_offset = -156</p></td></tr><tr><td>iso_9141_kwp_enable_reserved</td><td>Not Available</td></tr><tr><td>iso9141_kwp_settings_1</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_1</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination_1</td><td>Not Available</td></tr><tr><td>idle_wakeup_network_enables_1</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br></p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_2</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br></p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_3</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>OP_ETH1 : 4</td><td>OP_ETH2 : 5</td></tr><tr><td>OP_ETH3 : 6</td><td>OP_ETH4 : 7</td><td>OP_ETH5 : 8</td></tr><tr><td>OP_ETH6 : 9</td><td>OP_ETH7 : 10</td><td>OP_ETH8 : 11</td></tr><tr><td>OP_ETH9 : 12</td><td>OP_ETH10 : 13</td><td>OP_ETH11 : 14</td></tr><tr><td>OP_ETH12 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_3</td><td>Not Available</td></tr><tr><td>can_switch_mode</td><td>Not Available</td></tr><tr><td>text_api</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure">STextAPISettings</a> structure</td></tr><tr><td>pc_com_mode</td><td>Not Available</td></tr><tr><td>timeSyncSettings</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/timesync_icshardware_settings-structure">TIMESYNC_ICSHARDWARE_SETTINGS</a> structure</td></tr><tr><td>hwComLatencyTestEn</td><td>Not Available</td></tr><tr><td>reporting</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/rad_reporting_settings-structure">RAD_REPORTING_SETTINGS</a> structure</td></tr><tr><td>ethernet</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/ethernet_settings2-structure">ETHERNET_SETTINGS2</a> structure</td></tr><tr><td>gPTP</td><td>See <a href="https://docs.intrepidcs.com/neovi-api/win32-api-overview-intrepidcs-api/structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/sub-setting-structures-overview-intrepidcs-api/rad_gptp_settings-structure">RAD_GPTP_SETTINGS</a> structure</td></tr></tbody></table>
