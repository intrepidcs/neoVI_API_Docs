# SVCAN4IndSettings Structure

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   CAN_SETTINGS can1;
   CANFD_SETTINGS canfd1;
   CAN_SETTINGS can2;
   CANFD_SETTINGS canfd2;
   ETHERNET_SETTINGS ethernet;
   LIN_SETTINGS lin1;
   ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
   uint16_t iso_parity;
   uint16_t iso_msg_termination;
   uint32_t pwr_man_timeout;
   uint16_t pwr_man_enable;
   uint16_t perf_en;
   uint16_t iso15765_separation_time_offset;
   uint16_t network_enabled_on_boot;
   uint16_t network_enables;
   uint16_t network_enables_2;
   uint16_t network_enables_3;
   uint16_t Reserved;
   uint64_t termination_enables;
   uint32_t flags;
   ETHERNET_SETTINGS ethernet2;
}SVCAN4IndSettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SVCAN4IndSettings
   Dim can1 As CAN_SETTINGS
   Dim canfd1 As CANFD_SETTINGS
   Dim can2 As CAN_SETTINGS
   Dim canfd2 As CANFD_SETTINGS
   Dim ethernet As ETHERNET_SETTINGS
   Dim lin1 As LIN_SETTINGS
   Dim iso9141_kwp_settings As ISO9141_KEYWORD2000_SETTINGS
   Dim iso_parity As UInt16
   Dim iso_msg_termination As UInt16
   Dim pwr_man_timeout As UInt32
   Dim pwr_man_enable As UInt16
   Dim perf_en As UInt16
   Dim iso15765_separation_time_offset As UInt16
   Dim network_enabled_on_boot As UInt16
   Dim network_enables As UInt16
   Dim network_enables_2 As UInt16
   Dim network_enables_3 As UInt16
   Dim Reserved As UInt16
   Dim termination_enables As UInt64
   Dim flags As UInt32
   Dim ethernet2 As ETHERNET_SETTINGS
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SVCAN4IndSettings
{
   public CAN_SETTINGS can1;
   public CANFD_SETTINGS canfd1;
   public CAN_SETTINGS can2;
   public CANFD_SETTINGS canfd2;
   public ETHERNET_SETTINGS ethernet;
   public LIN_SETTINGS lin1;
   public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
   public UInt16 iso_parity;
   public UInt16 iso_msg_termination;
   public UInt32 pwr_man_timeout;
   public UInt16 pwr_man_enable;
   public UInt16 perf_en;
   public UInt16 iso15765_separation_time_offset;
   public UInt16 network_enabled_on_boot;
   public UInt16 network_enables;
   public UInt16 network_enables_2;
   public UInt16 network_enables_3;
   public UInt16 Reserved;
   public UInt64 termination_enables;
   public UInt32 flags;
   public ETHERNET_SETTINGS ethernet2;
}
```
{% endtab %}
{% endtabs %}

#### Remarks

<table><thead><tr><th width="401">Item</th><th>Description</th></tr></thead><tbody><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canfd2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>ethernet</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure.md">ETHERNET_SETTINGS</a> structure</td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>iso9141_kwp_settings</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTINGS</a> structure</td></tr><tr><td>iso_parity</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination</td><td>ISO9141 message termination setting:<br>0 - use inner frame time<br>1 - GME CIM-SCL</td></tr><tr><td>pwr_man_timeout</td><td><p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p></td></tr><tr><td>pwr_man_enable</td><td><p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p></td></tr><tr><td>perf_en</td><td>Performance test.?Default value = 0?</td></tr><tr><td>iso15765_separation_time_offset</td><td><p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.</p><p>Default value = 0</p><p>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p>ISO15765-2 Tx Message Inner frame spacing is what's specified in flow control message.- 998.4 us:<br>iso15765_separation_time_offset = -156</p></td></tr><tr><td>network_enabled_on_boot</td><td>Not Defined</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.<br></p><table><thead><tr><th>HSCAN : 0</th><th>MSCAN : 1</th><th>LIN1 : 2</th></tr></thead><tbody><tr><td>LIN2 : 3</td><td>NA : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>NA : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table><thead><tr><th>KLINE1 : 0</th><th>KLINE2 : 1</th><th>KLINE3 : 2</th></tr></thead><tbody><tr><td>KLINE4 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_3</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>NA : 4</td><td>NA : 5</td></tr><tr><td>NA : 6</td><td>NA : 7</td><td>NA : 8</td></tr><tr><td>NA : 9</td><td>NA : 10</td><td>NA : 11</td></tr><tr><td>NA : 12</td><td>NA : 13</td><td>NA : 14</td></tr><tr><td>NA : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>Reserved</td><td>Reserved</td></tr><tr><td>termination_enables</td><td><p>Bitfield containing the<br>termination enables. For the neoVI Fire 2, the termination is grouped<br>into banks. Only 2 form a single bank can be neabled.</p><table><thead><tr><th>HSCAN (Bank0): 0</th><th>MSCAN (Bank1): 1</th><th>HSCAN2 (BANK1) : 5</th></tr></thead><tbody><tr><td>HSCAN3 (Bank0) : 8</td><td>HSCAN4 (Bank1): 14</td><td>HSCAN5 (Bank0) : 15</td></tr><tr><td>HSCAN6 (Bank1) : 32</td><td>HSCAN7 (Bank0): 33</td><td></td></tr></tbody></table></td></tr><tr><td>flags</td><td>Not used</td></tr><tr><td>ethernet2</td><td>See ETHERNET_SETTINGS structure</td></tr></tbody></table>
