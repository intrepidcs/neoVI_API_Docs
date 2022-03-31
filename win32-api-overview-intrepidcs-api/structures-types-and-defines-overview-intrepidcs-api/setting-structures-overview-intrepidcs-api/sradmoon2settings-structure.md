# SRADMoon2Settings Structure

Structure defining the parameter in SRADMoon2Settings

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
  uint16_t perf_en;
  OP_ETH_GENERAL_SETTINGS opEthGen;
  OP_ETH_SETTINGS opEth1;
  uint16_t network_enables;
  uint16_t network_enables_2;
  uint16_t network_enabled_on_boot;
  uint16_t network_enables_3;
  STextAPISettings text_api;
  uint16_t pc_com_mode;
  TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
  uint16_t hwComLatencyTestEn;
}SRADMoon2Settings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SRADMoon2Settings
  Dim perf_en As UInt16
  Dim opEthGen As OP_ETH_GENERAL_SETTINGS
  Dim opEth1 As OP_ETH_SETTINGS
  Dim network_enables As UInt16
  Dim network_enables_2 As UInt16
  Dim network_enabled_on_boot As UInt16
  Dim network_enables_3 As UInt16
  Dim text_api As STextAPISettings
  Dim pc_com_mode As UInt16
  Dim timeSyncSettings As TIMESYNC_ICSHARDWARE_SETTINGS
  Dim hwComLatencyTestEn As UInt16
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SRADMoon2Settings
{
  public UInt16 perf_en;
  public OP_ETH_GENERAL_SETTINGS opEthGen;
  public OP_ETH_SETTINGS opEth1;
  public UInt16 network_enables;
  public UInt16 network_enables_2;
  public UInt16 network_enabled_on_boot;
  public UInt16 network_enables_3;
  public STextAPISettings text_api;
  public UInt16 pc_com_mode;
  public TIMESYNC_ICSHARDWARE_SETTINGS timeSyncSettings;
  public UInt16 hwComLatencyTestEn;
}
```
{% endtab %}

{% tab title="Python (ctype) Declare" %}
```python
class icsSpyMessage(ctypes.Structure):
   _pack_ = 2
   _fields_ = [
       ("perf_en",ctypes.c_ushort),
       ("opEthGen",OP_ETH_GENERAL_SETTINGS),
       ("opEth1",OP_ETH_SETTINGS),
       ("network_enables",ctypes.c_ushort),
       ("network_enables_2",ctypes.c_ushort),
       ("network_enabled_on_boot",ctypes.c_ushort),
       ("network_enables_3",ctypes.c_ushort),
       ("text_api",STextAPISettings),
       ("pc_com_mode",ctypes.c_ushort),
       ("timeSyncSettings",TIMESYNC_ICSHARDWARE_SETTINGS),
       ("hwComLatencyTestEn",ctypes.c_ushort),
       ]
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| perf\_en                   | Performance test. Default value = 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| opEthGen                   | See [OP\_ETH\_GENERAL\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/op\_eth\_general\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| opEth1                     | See [OP\_ETH\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/ethernet\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| network\_enables           | Not applicable for RAD SuperMoon. Set to 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| network\_enables\_2        | Not applicable for RAD SuperMoon. Set to 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| network\_enabled\_on\_boot | Not Available                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| network\_enables\_3        | <p>Bitfield containing the software license enables. Depending on the hardware license purchased the customer may have to conditionally select which hardware channels to enable. For example the neoVI Red license allows the user to enable any 2 Dual Wire CAN channels and any 2 LIN channels. To enable a specific network its corresponding bit must be set (1). In order to transmit or receive on a network it must be enabled.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>OP_Ethernet1 : 4</td><td>OP_Ethernet2 : 5</td></tr></tbody></table> |
| text\_api                  | See [STextAPISettings](sub-setting-structures-overview-intrepidcs-api/stextapisettings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| pc\_com\_mode              | Not Available                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| timeSyncSettings           | See [TIMESYNC\_ICSHARDWARE\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/timesync\_icshardware\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| hwComLatencyTestEn         | Not Available                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| gPTP                       | See [RAD\_GPTP\_SETTINGS](sub-setting-structures-overview-intrepidcs-api/rad\_gptp\_settings-structure.md) structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
