# SRADPlutoSettings Structure

This structure defines various settings for the RAD Pluto device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))

{
  unsigned short perf_en;
  CAN_SETTINGS can1;
  CANFD_SETTINGS canfd1;
  CAN_SETTINGS can2;
  CANFD_SETTINGS canfd2;
  LIN_SETTINGS lin1;
  unsigned short network_enables;
  unsigned short network_enables_2;
  unsigned short network_enables_3;
  uint64_t termination_enables;
  unsigned short misc_io_analog_enable;
  unsigned int pwr_man_timeout;
  unsigned short pwr_man_enable;
  unsigned short network_enabled_on_boot;
  unsigned short iso15765_separation_time_offset;
  unsigned short iso9141_kwp_enable_reserved;
  unsigned short iso_tester_pullup_enable;
  unsigned short iso_parity;
  unsigned short iso_msg_termination;
  ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_1;
  ETHERNET_SETTINGS ethernet;
  STextAPISettings text_api;
  unsigned int Flags;
  SPluto_CustomParams custom;
}SRADPlutoSettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SRADPlutoSettings
  Dim perf_en As UInt16
  Dim can1 As CAN_SETTINGS
  Dim canfd1 As CANFD_SETTINGS
  Dim can2 As CAN_SETTINGS
  Dim canfd2 As CANFD_SETTINGS
  Dim lin1 As LIN_SETTINGS
  Dim network_enables As UInt16
  Dim network_enables_2 As UInt16
  Dim network_enables_3 As UInt16
  Dim termination_enables As UInt64
  Dim misc_io_analog_enable As UInt16
  Dim pwr_man_timeout As UInt32
  Dim pwr_man_enable As UInt16
  Dim network_enabled_on_boot As UInt16
  Dim iso15765_separation_time_offset As UInt16
  Dim iso9141_kwp_enable_reserved As UInt16
  Dim iso_tester_pullup_enable As UInt16
  Dim iso_parity As UInt16
  Dim iso_msg_termination As UInt16
  Dim iso9141_kwp_settings_1 As ISO9141_KEYWORD2000_SETTINGS
  Dim ethernet As ETHERNET_SETTINGS
  Dim text_api As STextAPISettings
  Dim Flags As UInt32
  Dim custom As SPluto_CustomParams
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SRADPlutoSettings
{
public UInt16 perf_en;
public CAN_SETTINGS can1;
public CANFD_SETTINGS canfd1;
public CAN_SETTINGS can2;
public CANFD_SETTINGS canfd2;
public LIN_SETTINGS lin1;
public UInt16 network_enables;
public UInt16 network_enables_2;
public UInt16 network_enables_3;
public UInt64 termination_enables;
public UInt16 misc_io_analog_enable;
public UInt32 pwr_man_timeout;
public UInt16 pwr_man_enable;
public UInt16 network_enabled_on_boot;
public UInt16 iso15765_separation_time_offset;
public UInt16 iso9141_kwp_enable_reserved;
public UInt16 iso_tester_pullup_enable;
public UInt16 iso_parity;
public UInt16 iso_msg_termination;
public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings_1;
public ETHERNET_SETTINGS ethernet;
public STextAPISettings text_api;
public UInt32 Flags;
public SPluto_CustomParams custom;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

<table><thead><tr><th width="414"></th><th>Description</th></tr></thead><tbody><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>LIN1 : 2</td><td>HSCAN2 : 5</td></tr></tbody></table></td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Ethernet : 13</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_3</td><td>Not used. Set to 0</td></tr><tr><td>termination_enables</td><td><p>Bitfield containing the termination enables.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>HSCAN2 : 5</td></tr></tbody></table></td></tr><tr><td>misc_io_analog_enable</td><td>Not Used, set to 0.</td></tr><tr><td>pwr_man_timeout</td><td><p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p></td></tr><tr><td>pwr_man_enable</td><td><p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p></td></tr><tr><td>network_enabled_on_boot</td><td><p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0</p></td></tr><tr><td>iso15765_separation_time_offset</td><td><p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.<br></p><p>Default value = 0</p><p><br>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p><br>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p><br>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.- 998.4 us: iso15765_separation_time_offset = -156</p></td></tr><tr><td>iso9141_kwp_enable_reserved</td><td>Reserved</td></tr><tr><td>iso_tester_pullup_enable</td><td>Not used Set to 0</td></tr><tr><td>iso_parity</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination</td><td>ISO9141 message termination setting: 0 - use inner frame time 1 - GME CIM-SCL</td></tr><tr><td>iso9141_kwp_settings_1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>ethernet</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure.md">ETHERNET_SETTINGS</a> structure</td></tr><tr><td>text_api</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> structure</td></tr><tr><td>Flags</td><td>Set to 0</td></tr><tr><td>custom</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/spluto_customparams-structure.md">SPluto_CustomParams</a> structure</td></tr></tbody></table>
