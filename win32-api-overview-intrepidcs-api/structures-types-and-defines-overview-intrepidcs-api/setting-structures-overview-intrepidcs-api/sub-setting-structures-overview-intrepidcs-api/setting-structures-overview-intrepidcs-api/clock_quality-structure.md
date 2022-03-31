# clock\_quality Structure

This structure defines various settings for the clock\_quality in gPTP

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
// Some typedef struct __declspec (align(1))
{
   uint8_t clock_class;
   uint8_t clock_accuracy;
   uint16_t offset_scaled_log_variance;
}clock_quality;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=1)> Public Structure clock_quality
   Dim clock_class As Byte
   Dim clock_accuracy As Byte
   Dim offset_scaled_log_variance As UInt16
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=1)]
public struct clock_quality
{
   public byte clock_class;
   public byte clock_accuracy;
   public UInt16 offset_scaled_log_variance;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                          | Description                                                                                                                                                                                        |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| clock\_class                  | <p>Clock Class indicates the traceability of the data from the ClockMaster when it acts as a GrandMaster.</p><p>See IEEE Std 1588-2019 for a more detailed description of clockClass.</p>          |
| clock\_accuracy               | <p>Sets the expected time accuracy of the ClockMaster. Lower values indicate better accuracy. 254 is for Unknown.</p><p>See IEEE Std 1588-2019 for more detailed description of clockAccuracy.</p> |
| offset\_scaled\_log\_variance | <p>This parameter is an estimate of the Variance in PTP.</p><p>See gPTP spec, 8021AS for more details.</p>                                                                                         |
