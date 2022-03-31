---
cover: ../../../../.gitbook/assets/new-cover-image.png
coverY: 0
---

# STextAPISettings Structure

This structure defines settings for Text API communication for neoVI Fire devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct _STextAPISettings
{
    unsigned int can1_tx_id;
    unsigned int can1_rx_id;
    unsigned int can1_options;// Set to 1 for Extended, 0 for standard
    unsigned int can2_tx_id;
    unsigned int can2_rx_id;
    unsigned int can2_options; // Set to 1 for Extended, 0 for standard
    unsigned int network_enables;
    unsigned int can3_tx_id3;
    unsigned int can3_rx_id3;
    unsigned int can3_options; // Set to 1 for Extended, 0 for standard
    unsigned int can4_tx_id4;
    unsigned int can4_rx_id4;
    unsigned int can4_options; // Set to 1 for Extended, 0 for standard
    int Reserved0;
    int Reserved1;
    int Reserved2;
    int Reserved3;
    int Reserved4;
}STextAPISettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure STextAPISettings
    Dim can1_tx_id As UInt32
    Dim can1_rx_id As UInt32
    Dim can1_options As UInt32 '// Set to 1 for Extended, 0 for standard
    Dim can2_tx_id As UInt32
    Dim can2_rx_id As UInt32
    Dim can2_options As UInt32 '// Set to 1 for Extended, 0 for standard
    Dim network_enables As UInt32
    Dim can3_tx_id3 As UInt32
    Dim can3_rx_id3 As UInt32
    Dim can3_options As UInt32 '// Set to 1 for Extended, 0 for standard
    Dim can4_tx_id4 As UInt32
    Dim can4_rx_id4 As UInt32
    Dim can4_options As UInt32 '// Set to 1 for Extended, 0 for standard
    Dim Reserved0 As Int32
    Dim Reserved1 As Int32
    Dim Reserved2 As Int32
    Dim Reserved3 As Int32
    Dim Reserved4 As Int32
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct STextAPISettings
{
    public UInt32 can1_tx_id;
    public UInt32 can1_rx_id;
    public UInt32 can1_options; // Set to 1 for Extended, 0 for standard
    public UInt32 can2_tx_id;
    public UInt32 can2_rx_id;
    public UInt32 can2_options; // Set to 1 for Extended, 0 for standard
    public UInt32 network_enables;
    public UInt32 can3_tx_id3;
    public UInt32 can3_rx_id3;
    public UInt32 can3_options; // Set to 1 for Extended, 0 for standard
    public UInt32 can4_tx_id4;
    public UInt32 can4_rx_id4;
    public UInt32 can4_options; // Set to 1 for Extended, 0 for standard
    public Int32 Reserved0;
    public Int32 Reserved1;
    public Int32 Reserved2;
    public Int32 Reserved3;
    public Int32 Reserved4;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                                            | Description                                                                                                                                                                                                                                                                                                                                                 |
| --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [icscm\_uint32](../intrepid-api-data-types.md) can\_tx\_id      | Sets or Reads the Arbitration ID for Sending Text API commands                                                                                                                                                                                                                                                                                              |
| [icscm\_uint32](../intrepid-api-data-types.md) can\_rx\_id      | Sets or Reads the Arbitration ID for Sending Receiving API commands                                                                                                                                                                                                                                                                                         |
| [icscm\_uint32](../intrepid-api-data-types.md) can\_options     | Sets the length of the Arbitration ID’s. Set to 1 for Extended and 0 for Standard                                                                                                                                                                                                                                                                           |
| [icscm\_uint32](../intrepid-api-data-types.md) network\_Enables | <p>Bitfield telling which netowrk to support Text API. One one can be enabled at a time.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>HS CAN : 1</td><td>MS CAN : 2</td></tr><tr><td>HS CAN 2 : 32</td><td>HS CAN 3 : 256</td></tr><tr><td>RS232/UART2 : 4194304</td><td>UART1 : 2097152</td></tr></tbody></table> |
| [icscm\_uint32](../intrepid-api-data-types.md) Reserved         | Not used                                                                                                                                                                                                                                                                                                                                                    |
