# SVCAN412Settings Structure

This structure defines various settings for the ValueCAN4-1 and ValueCAN4-2 devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{

int64_t perf_en;
CAN_SETTINGS can1;
CANFD_SETTINGS canfd1;
CAN_SETTINGS can2;
CANFD_SETTINGS canfd2;
uint64_t network_enables;
uint64_t termination_enables;
uint32_t pwr_man_timeout;
uint16_t pwr_man_enable;
uint16_t network_enabled_on_boot;
uint16_t iso15765_separation_time_offset;
STextAPISettings text_api;
uint32_t flags;
}

SVCAN412Settings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SVCAN412Settings
Dim perf_en As Int64
Dim can1 As CAN_SETTINGS
Dim canfd1 As CANFD_SETTINGS
Dim can2 As CAN_SETTINGS
Dim canfd2 As CANFD_SETTINGS
Dim network_enables As UInt64
Dim termination_enables As UInt64
Dim pwr_man_timeout As UInt32
Dim pwr_man_enable As UInt16
Dim network_enabled_on_boot As UInt16
Dim iso15765_separation_time_offset As UInt16
Dim text_api As STextAPISettings
Dim flags As UInt32
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SVCAN412Settings
{
public Int64 perf_en;
public CAN_SETTINGS can1;
public CANFD_SETTINGS canfd1;
public CAN_SETTINGS can2;
public CANFD_SETTINGS canfd2;
public UInt64 network_enables;
public UInt64 termination_enables;
public UInt32 pwr_man_timeout;
public UInt16 pwr_man_enable;
public UInt16 network_enabled_on_boot;
public UInt16 iso15765_separation_time_offset;
public STextAPISettings text_api;
public UInt32 flags;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| perf\_en                           | Performance test. Default value = 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| can1                               | See [CAN\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/can\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| canfd1                             | See [CANFD\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/canfd\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| can2                               | See [CAN\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/can\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| canfd2                             | See [CANFD\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/canfd\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| network\_enables                   | <p>Bitfield containing the software license enables. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : Bit 0</td><td>HSCAN2 : Bit 5</td></tr></tbody></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| termination\_enables               | <p>Bitfield containing the enables for CAN Termination. To enable a specific channel its corresponding bit must be set (1). .</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HSCAN : Bit 0</td><td>HSCAN2 : Bit 5</td></tr></tbody></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| pwr\_man\_timeout                  | <p>Number of milliseconds of no bus activity required before neoVI enters low power mode. Note pwr_man_enable must be set for power management to be enabled.</p><p>Default value = 10000</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| pwr\_man\_enable                   | <p>1 = enable Power Management, 0 = disable.</p><p>Default value = 0</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| network\_enabled\_on\_boot         | <p>Normally neoVI only initiates its comm channels when CoreMini is running or if neoVI is online with DLL/Vehicle Spy 3. Practically this means the the CAN controllers stay in Listen Only mode until the device goes online. Once online the neoVI loads the user settings. Setting this parameter to 1 will change this behavior so that the neoVI enables its controllers immediately on boot.</p><p>Default value = 0</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| iso15765\_separation\_time\_offset | <p>In an ISO15765-2 Transmission, the receiver transmits a flow control message that informs that transmitter how much time there should be between individual CAN messages. This parameter allows the user to shift that spacing to make it smaller or larger. Valid range is -1563 to 1563 units where each unit represents 6.4us. Defaults to 0. If IFS plus the offset is negative than the Tx Messages will be back to back.</p><p>Default value = 0</p><p>Examples:</p><p>ISO15765-2 Tx Message Inner frame spacing is exactly what is specified in flow control message: iso15765_separation_time_offset = 0</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.+ 998.4 us: iso15765_separation_time_offset = 156</p><p>ISO15765-2 Tx Message Inner frame spacing is what’s specified in flow control message.- 998.4 us: iso15765_separation_time_offset = -156</p> |
| text\_api                          | See [STextAPISettings](sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| flags                              | <p>Bitfield with misc settings for the device. List below gives the parameter with the bit number to have set to enable.</p><p>Disable USB Check On Boot : 0</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
