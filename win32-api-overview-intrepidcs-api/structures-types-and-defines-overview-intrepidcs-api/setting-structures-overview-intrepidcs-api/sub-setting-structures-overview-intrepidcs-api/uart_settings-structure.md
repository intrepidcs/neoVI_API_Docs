# UART\_SETTINGS Structure

This structure defines settings for UART access on neoVI Fire devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct _UART_SETTINGS{
   unsigned short Baudrate;
   unsigned short spbrg;
   unsigned short brgh;
   unsigned short parity;
   unsigned short stop_bits;
   unsigned char flow_control; // 0- off, 1 - Simple CTS RTS,
   unsigned char reserved_1;
   unsigned int bOptions; //AND to combind these values invert_tx = 1 invert_rx = 2 half_duplex = 4
} UART_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```visual-basic
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure UART_SETTINGS
   Dim Baudrate As UInt16
   Dim spbrg As UInt16
   Dim brgh As UInt16
   Dim parity As UInt16
   Dim stop_bits As UInt16
   Dim flow_control As Byte '// 0- off, 1 - Simple CTS RTS,
   Dim reserved_1 As Byte
   Dim bOptions As UInt32 '//AND to combind these values invert_tx = 1 invert_rx = 2 half_duplex = 4
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct UART_SETTINGS
{
   public UInt16 Baudrate; If
   public UInt16 spbrg;
   public UInt16 brgh;
   public UInt16 parity;
   public UInt16 stop_bits;
   public byte flow_control; // 0- off, 1 - Simple CTS RTS,
   public byte reserved_1;
   public UInt32 bOptions; //AND to combind these values invert_tx = 1 invert_rx = 2 half_duplex = 4
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                                        | Description                                                                                                                                                                                                                                         |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [icscm\_uint16](../intrepid-api-data-types.md) Baudrate     | Holds the baud rate for the UART Connection. An example value could be 10417 or 9600                                                                                                                                                                |
| [icscm\_uint16](../intrepid-api-data-types.md) spbrg        |                                                                                                                                                                                                                                                     |
| [icscm\_uint16](../intrepid-api-data-types.md) brgh         |                                                                                                                                                                                                                                                     |
| [icscm\_uint16](../intrepid-api-data-types.md) parity       | <p>Sets the Parity type. Valid values are below</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>None</td><td>0</td></tr><tr><td>Even</td><td>1</td></tr><tr><td>Odd</td><td>2</td></tr></tbody></table>       |
| [icscm\_uint16](../intrepid-api-data-types.md) stop\_bits   | <p>Sets the number of stop bits to use. Valid values are below.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>One Stop Bit</td><td>1</td></tr><tr><td>Two Stop Bits</td><td>2</td></tr></tbody></table>     |
| [icscm\_uint8](../intrepid-api-data-types.md) flow\_control | Set to 0 for no flow control and 1 for simple CTS RTS                                                                                                                                                                                               |
| [icscm\_uint8](../intrepid-api-data-types.md) reserved      |                                                                                                                                                                                                                                                     |
| [icscm\_uint32](../intrepid-api-data-types.md) bOptions     | <p>Bitfield containing UART Options</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Invert Tx</td><td>1</td></tr><tr><td>Invert Rx</td><td>2</td></tr><tr><td>Half Duplex</td><td>4</td></tr></tbody></table> |
