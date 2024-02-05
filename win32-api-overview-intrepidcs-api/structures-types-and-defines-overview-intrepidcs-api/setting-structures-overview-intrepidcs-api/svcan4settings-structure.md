# SVCAN4Settings Structure

This structure defines various settings for the ValueCAN 4-4 and 4-2EL device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec
{
  uint16_t perf_en;
  CAN_SETTINGS can1;
  CANFD_SETTINGS canFD1;
  CAN_SETTINGS can2;
  CANFD_SETTINGS canFD2;
  CAN_SETTINGS can3;
  CANFD_SETTINGS canFD3;
  CAN_SETTINGS can4;
  CANFD_SETTINGS canFD4;
  unsigned short network_enables;
  unsigned short network_enables_2;
  LIN_SETTINGS lin1;
  unsigned short network_enabled_on_boot;
  unsigned short iso_9141_kwp_enable_reserved;
  ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
  unsigned short iso_parity;
  unsigned short iso_msg_termination_1;
  unsigned short network_enables_3;
  STextAPISettings text_api;
  ETHERNET_SETTINGS ethernet;
  unsigned int Flags;
  unsigned short pwr_man_enable;
  unsigned short pwr_man_timeout;
}
SVCAN4Settings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SVCAN4Settings
  Dim perf_en As UInt16
  Dim can1 As CAN_SETTINGS
  Dim canFD1 As CANFD_SETTINGS
  Dim can2 As CAN_SETTINGS
  Dim canFD2 As CANFD_SETTINGS
  Dim can3 As CAN_SETTINGS
  Dim canFD3 As CANFD_SETTINGS
  Dim can4 As CAN_SETTINGS
  Dim canFD4 As CANFD_SETTINGS
  Dim network_enables As UInt16
  Dim network_enables_2 As UInt16
  Dim lin1 As LIN_SETTINGS
  Dim network_enabled_on_boot As UInt16
  Dim iso_9141_kwp_enable_reserved As UInt16
  Dim iso9141_kwp_settings As ISO9141_KEYWORD2000_SETTINGS
  Dim iso_parity As UInt16
  Dim iso_msg_termination_1 As UInt16
  Dim network_enables_3 As UInt16
  Dim text_api As STextAPISettings
  Dim ethernet As ETHERNET_SETTINGS
  Dim Flags As UInt32
  Dim pwr_man_enable As UInt16
  Dim pwr_man_timeout As UInt16
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SVCAN4Settings
{
public UInt16 perf_en;
public CAN_SETTINGS can1;
public CANFD_SETTINGS canFD1;
public CAN_SETTINGS can2;
public CANFD_SETTINGS canFD2;
public CAN_SETTINGS can3;
public CANFD_SETTINGS canFD3;
public CAN_SETTINGS can4;
public CANFD_SETTINGS canFD4;
public UInt16 network_enables;
public UInt16 network_enables_2;
public LIN_SETTINGS lin1;
public UInt16 network_enabled_on_boot;
public UInt16 iso_9141_kwp_enable_reserved;
public ISO9141_KEYWORD2000_SETTINGS iso9141_kwp_settings;
public UInt16 iso_parity;
public UInt16 iso_msg_termination_1;
public UInt16 network_enables_3;
public STextAPISettings text_api;
public ETHERNET_SETTINGS ethernet;
public UInt32 Flags;
public UInt16 pwr_man_enable;
public UInt16 pwr_man_timeout;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

<table><thead><tr><th width="266">Item</th><th>Description</th></tr></thead><tbody><tr><td>perf_en</td><td>Performance test. Default value = 0</td></tr><tr><td>can1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canFD1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canFD2</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canFD3</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>can4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/can_settings-structure.md">CAN_SETTINGS</a> structure</td></tr><tr><td>canFD4</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/canfd_settings-structure.md">CANFD_SETTINGS</a> structure</td></tr><tr><td>network_enables</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : 0</td><td>MSCAN : 1</td><td>LIN1 : 2</td></tr><tr><td>LIN2 : 3</td><td>VIRTUAL : 4</td><td>HSCAN2 : 5</td></tr><tr><td>LSFTCAN1 : 6</td><td>SWCAN1 : 7</td><td>HSCAN3 : 8</td></tr><tr><td>GMCGI : 9</td><td>J1850 : 10</td><td>LIN3 : 11</td></tr><tr><td>LIN4 : 12</td><td>J1708 : 13</td><td>HSCAN4 : 14</td></tr><tr><td>HSCAN5 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>network_enables_2</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>KLINE1 : 0</td><td>KLINE2 : 1</td><td>KLINE3 : 2</td></tr><tr><td>KLINE4 : 3</td><td>FLEXRAY1A : 4</td><td>UART : 5</td></tr><tr><td>UART2 : 6</td><td>LIN5 : 7</td><td>MOST25 : 8</td></tr><tr><td>MOST50 : 9</td><td>FLEXRAY1B : 10</td><td>SWCAN2 : 11</td></tr><tr><td>ETHERNET_DAQ : 12</td><td>ETHERNET : 13</td><td>FLEXRAY2A : 14</td></tr><tr><td>FLEXRAY2B : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>lin1</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/lin_settings-structure.md">LIN_SETTINGS</a> structure</td></tr><tr><td>network_enabled_on_boot</td><td><p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0</p></td></tr><tr><td>iso_9141_kwp_enable_reserved</td><td>Reserved</td></tr><tr><td>iso9141_kwp_settings</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/iso9141_keyword2000_settings-structure.md">ISO9141_KEYWORD2000_SETTING</a>S structure</td></tr><tr><td>iso_parity</td><td>ISO9141 Parity setting: 0 - no parity, 1 - even, 2 - odd</td></tr><tr><td>iso_msg_termination_1</td><td>ISO9141 message termination setting: 0 - use inner frame time 1 - GME CIM-SCL</td></tr><tr><td>network_enables_3</td><td><p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>HSCAN6 : 0</td><td>HSCAN7 : 1</td><td>LIN6 : 2</td></tr><tr><td>LSFTCAN2 : 3</td><td>OP_ETH1 : 4</td><td>OP_ETH2 : 5</td></tr><tr><td>OP_ETH3 : 6</td><td>OP_ETH4 : 7</td><td>OP_ETH5 : 8</td></tr><tr><td>OP_ETH6 : 9</td><td>OP_ETH7 : 10</td><td>OP_ETH8 : 11</td></tr><tr><td>OP_ETH9 : 12</td><td>OP_ETH10 : 13</td><td>OP_ETH11 : 14</td></tr><tr><td>OP_ETH12 : 15</td><td></td><td></td></tr></tbody></table></td></tr><tr><td>text_api</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md">STextAPISettings</a> structure</td></tr><tr><td>ethernet</td><td>See <a href="sub-setting-structures-overview-intrepidcs-api/ethernet_settings-structure.md">ETHERNET_SETTINGS</a> structure</td></tr><tr><td>Flags</td><td>Not used</td></tr><tr><td>pwr_man_enable</td><td><p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p></td></tr><tr><td>pwr_man_timeout</td><td><p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p></td></tr></tbody></table>

