# RAD\_REPORTING\_SETTINGS Structure

**Setting structure for reporting options for the Rad Galaxy**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint32_t flags;
   uint16_t temp_interval_ms;
   uint16_t gps_interval_ms;
   uint16_t serdes_interval_ms;
   uint16_t io_interval_ms;
   uint32_t rsvd;
}RAD_REPORTING_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure RAD_REPORTING_SETTINGS
   Dim flags As UInt32
   Dim temp_interval_ms As UInt16
   Dim gps_interval_ms As UInt16
   Dim serdes_interval_ms As UInt16
   Dim io_interval_ms As UInt16
   Dim rsvd As UInt32
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct RAD_REPORTING_SETTINGS
{
   public UInt32 flags;
   public UInt16 temp_interval_ms;
   public UInt16 gps_interval_ms;
   public UInt16 serdes_interval_ms;
   public UInt16 io_interval_ms;
   public UInt32 rsvd;
}
```
{% endtab %}
{% endtabs %}

#### Remarks

| Item                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| flags                | <p>Bitfield for enabling different IO features. </p><table><thead><tr><th>I/O Feature</th><th>Bit to set</th></tr></thead><tbody><tr><td>TEMP ENABLE</td><td>0x0001</td></tr><tr><td>MIC2 GPS_ENABLE</td><td>0x0002</td></tr><tr><td>INT GPS_ENABLE</td><td>0x0004</td></tr><tr><td>MIC2 GPS_ENABLE2</td><td>0x0008</td></tr><tr><td>MISC1 DIN</td><td>0x0010</td></tr><tr><td>MISC2 DIN</td><td>0x0020</td></tr><tr><td>MISC1 PWMIN</td><td>0x0040</td></tr><tr><td>MISC2 PWMIN</td><td>0x0080</td></tr><tr><td>AIN1</td><td>0x0100</td></tr><tr><td>SERDES ENABLE</td><td>0x0200</td></tr></tbody></table> |
| temp\_interval\_ms   | Sets the interval in ms for reporting the temperature.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| gps\_interval\_ms    | Sets the interval in ms for reporting the GPS.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| serdes\_interval\_ms | Sets the interval in ms for reporting the Serdes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| io\_interval\_ms     | Sets the interval in ms for reporting the IO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| rsvd                 | <p>Reserved<br></p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
