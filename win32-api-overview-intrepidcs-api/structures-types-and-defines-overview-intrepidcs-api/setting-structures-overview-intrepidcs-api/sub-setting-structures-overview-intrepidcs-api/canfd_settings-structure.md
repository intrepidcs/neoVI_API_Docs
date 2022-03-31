# CANFD\_SETTINGS Structure

This structure defines settings for CANFD networks on supporting neoVI and ValueCAN devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
    unsigned char FDMode;
    unsigned char FDBaudrate;
    unsigned char FDTqSeg1;
    unsigned char FDTqSeg2;
    unsigned char FDTqProp;
    unsigned char FDTqSync;
    unsigned short FDBRP;
    unsigned char FDTDC;
    unsigned char reserved;
}CANFD_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure CANFD_SETTINGS
   Dim FDMode As Byte
   Dim FDBaudrate As Byte
   Dim FDTqSeg1 As Byte
   Dim FDTqSeg2 As Byte
   Dim FDTqProp As Byte
   Dim FDTqSync As Byte
   Dim FDBRP As UInt16
   Dim FDTDC As Byte
   Dim reserved As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
 public struct CANFD_SETTINGS
 {
 public byte FDMode;
 public byte FDBaudrate;
 public byte FDTqSeg1;
 public byte FDTqSeg2;
 public byte FDTqProp;
 public byte FDTqSync;
 public UInt16 FDBRP;
 public byte FDTDC;
 public byte reserved;
 }
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FDMode     | <p>Sets the CANFD Mode in the device. Table below lists the options.</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Mode</td><td>Value</td></tr><tr><td>NO_CANFD</td><td>0</td></tr><tr><td>CANFD_ENABLED</td><td>1</td></tr><tr><td>CANFD_BRS_ENABLED</td><td>2</td></tr><tr><td>CANFD_ENABLED_ISO</td><td>3</td></tr><tr><td>CANFD_BRS_ENABLED_ISO</td><td>4</td></tr></tbody></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| FDBaudrate | <p>Bit rate to use. The value is enumerated from a commonly used list of rates. The table below lists the rates</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Rate</td><td>Value</td></tr><tr><td>20000</td><td>0</td></tr><tr><td>33333</td><td>1</td></tr><tr><td>50000</td><td>2</td></tr><tr><td>62500</td><td>3</td></tr><tr><td>83333</td><td>4</td></tr><tr><td>100000</td><td>5</td></tr><tr><td>125000</td><td>6</td></tr><tr><td>250000</td><td>7</td></tr><tr><td>500000</td><td>8</td></tr><tr><td>800000</td><td>9</td></tr><tr><td>1000000</td><td>10</td></tr><tr><td>666000</td><td>11</td></tr><tr><td>2000000</td><td>12</td></tr><tr><td>4000000</td><td>13</td></tr><tr><td>5000000</td><td>14</td></tr><tr><td>6667000</td><td>15</td></tr><tr><td>8000000</td><td>16</td></tr><tr><td>10000000</td><td>17</td></tr></tbody></table> |
| FDTqSeg1   | Phase segment 1 value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FDTqSeg2   | Phase segment 2 value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FDTqProp   | Propagation delay                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| FDTqSync   | Syncro jump width                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| FDBRP      | Baud Rate Presale                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| FDTDC      | Transceiver delay compensation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| reserved   | Reserved, set to 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
