# SVCANRFSettings Structure

This structure defines various settings for the ValueCAN RF device

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
CAN_SETTINGS can1;
CAN_SETTINGS can2;
CAN_SETTINGS can3;
CAN_SETTINGS can4;
LIN_SETTINGS lin1;
LIN_SETTINGS lin2;
unsigned short network_enables;
unsigned short network_enabled_on_boot;
unsigned int pwr_man_timeout;
unsigned short pwr_man_enable;
unsigned short misc_io_initial_ddr;
unsigned short misc_io_initial_latch;
unsigned short misc_io_analog_enable;
unsigned short misc_io_report_period;
unsigned short misc_io_on_report_events;
unsigned short iso15765_separation_time_offset;
ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
unsigned short perf_en;
unsigned short iso_parity;
unsigned short iso_msg_termination;
unsigned short iso_tester_pullup_enable;
unsigned short network_enables_2;
ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_2;
unsigned short iso_parity_2;
unsigned short iso_msg_termination_2;
unsigned short idle_wakeup_network_enables_1;
unsigned short idle_wakeup_network_enables_2;
unsigned short disableFwLEDs;
}SVCANRFSettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SVCANRFSettings
Dim can1 As CAN_SETTINGS
Dim can2 As CAN_SETTINGS
Dim can3 As CAN_SETTINGS
Dim can4 As CAN_SETTINGS
Dim lin1 As LIN_SETTINGS
Dim lin2 As LIN_SETTINGS
Dim network_enables As UInt16
Dim network_enabled_on_boot As UInt16
Dim pwr_man_timeout As UInt32
Dim pwr_man_enable As UInt16
Dim misc_io_initial_ddr As UInt16
Dim misc_io_initial_latch As UInt16
Dim misc_io_analog_enable As UInt16
Dim misc_io_report_period As UInt16
Dim misc_io_on_report_events As UInt16
Dim iso15765_separation_time_offset As UInt16
Dim iso9141_kwp_settings As ISO9141_KEYWORD2000_SETTINGS
Dim perf_en As UInt16
Dim iso_parity As UInt16
Dim iso_msg_termination As UInt16
Dim iso_tester_pullup_enable As UInt16
Dim network_enables_2 As UInt16
Dim iso9141_kwp_settings_2 As ISO9141_KEYWORD2000_SETTINGS
Dim iso_parity_2 As UInt16
Dim iso_msg_termination_2 As UInt16
Dim idle_wakeup_network_enables_1 As UInt16
Dim idle_wakeup_network_enables_2 As UInt16
Dim disableFwLEDs As UInt16
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SVCANRFSettings
{
public CAN_SETTINGS can1;
public CAN_SETTINGS can2;
public CAN_SETTINGS can3;
public CAN_SETTINGS can4;
public LIN_SETTINGS lin1;
public LIN_SETTINGS lin2;
public UInt16 network_enables;
public UInt16 network_enabled_on_boot;
public UInt32 pwr_man_timeout;
public UInt16 pwr_man_enable;
public UInt16 misc_io_initial_ddr;
public UInt16 misc_io_initial_latch;
public UInt16 misc_io_analog_enable;
public UInt16 misc_io_report_period;
public UInt16 misc_io_on_report_events;
public UInt16 iso15765_separation_time_offset;
public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
public UInt16 perf_en;
public UInt16 iso_parity;
public UInt16 iso_msg_termination;
public UInt16 iso_tester_pullup_enable;
public UInt16 network_enables_2;
public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_2;
public UInt16 iso_parity_2;
public UInt16 iso_msg_termination_2;
public UInt16 idle_wakeup_network_enables_1;
public UInt16 idle_wakeup_network_enables_2;
public UInt16 disableFwLEDs;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

<table><thead><tr><th width="412">Item</th><th>Description</th></tr></thead><tbody><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>can3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>can4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>lin2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 :15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enabled_on_boot</td><td><p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0</p></td></tr><tr><td>pwr_man_timeout</td><td><p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p></td></tr><tr><td>pwr_man_enable</td><td><p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p></td></tr><tr><td>misc_io_initial_ddr</td><td><p>MISC IO Initial Data Direction Register. Controls the initial data direction of the tri-states on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an input and bit value 1 signifies and output. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC1 to be output, all else input: misc_io_initial_ddr = 1</p><p>Set MISC1and MISC2 to be output, all else input: misc_io_initial_ddr = 3 (11 binary)</p><p>Set all MISC pins to output: misc_io_initial_ddr = 65535 (1111111111111111 binary)</p></td></tr><tr><td>misc_io_initial_latch</td><td><p>MISC IO Initial Latch Register. Controls the initial output latch value on all misc digital pins. Each bit corresponds to an individual misc pin. Bit value of 0 signifies an low voltage and bit value 1 signifies high voltage. Bit values corresponding to non existent pins (EX MISC7-MISC15 on FIRE) have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC1 to be high, all else low: misc_io_initial_latch = 1</p><p>Set MISC1and MISC2 to be high, all else low: misc_io_initial_latch = 3 (11 binary)</p><p>Set all MISC pins to high: misc_io_initial_latch = 65535 (1111111111111111 binary)</p><p>Note: In order for digital outputs to work correctly the corresponding bit in misc_io_initial_ddr must be set to output and corresponding bit in misc_io_analog_enable must be cleared.</p></td></tr><tr><td>misc_io_analog_enable</td><td><p>MISC IO Analog Enable Register. Controls the initial analog enables on all misc analog pins. Each bit corresponds to an individual misc pin that supports analog input. Bit value of 0 signifies that corresponding misc pin is digital only, and bit value 1 signifies corresponding misc pin is analog. Note that because some MISC pins are not capable of analog they are not included in the register. For example neoVI FIRE’s analog pins are MISC3-MISC6, therefore bit 0 corresponds to MISC3’s analog enable. Bit values corresponding to non existent pins have no effect.</p><p>Default value = 0</p><p>Examples:</p><p>Set MISC3 to be analog, all else digital. (neoVI FIRE) : misc_io_analog_enable = 1</p><p>Set MISC3 and MISC4 to be analog, all else digital. (neoVI FIRE): misc_io_analog_enable = 3 (11 binary)</p><p>Set all MISC pins to high: misc_io_analog_enable = 65535 (1111111111111111 binary) Note: that in order for analog inputs to work correctly the corresponding bit in misc_io_analog_enable must be set to 1.</p></td></tr><tr><td>misc_io_report_period</td><td><p>Period in milliseconds of device report message holding digital and analog data.</p><p>Default value = 100</p><p>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</p></td></tr><tr><td>misc_io_on_report_events</td><td><p>Period in milliseconds of device report message holding digital and analog data.</p><p>Default value = 100</p><p>Note: Periodic reporting requires misc_io_on_report_events[0] to be set.</p></td></tr><tr><td>iso15765_separation_time_offset</td><td><p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.</p><p>Default value = 0</p><p>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.- 998.4 us: iso15765_separation_time_offset = -156</p></td></tr><tr><td>iso9141_kwp_settings</td><td>See ISO9141_KEYWORD2000_SETTINGS structure</td></tr><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>iso_parity</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination</td><td>ISO9141 message termination setting: 0 - use inner frame time 1 - GME CIM-SCL</td></tr><tr><td>iso_tester_pullup_enable</td><td>Not Available</td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 :6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B :15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>iso9141_kwp_settings_2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity_2</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination_2</td><td>ISO9141 message termination setting: 0 - use inner frame time 1 - GME CIM-SCL</td></tr><tr><td>idle_wakeup_network_enables_1</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>idle_wakeup_network_enables_2</td><td><p>Bitfield containing list of hardware networks to look at for sleep enable. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 :6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B :15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>disableFwLEDs</td><td>Disables the LEDs on the device.</td></tr></tbody></table>

