# timestamp Structure

This structure defines Timestamp from gPTP

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(1))
{
   uint16_t seconds_msb;
   uint32_t seconds_lsb;
   uint32_t nanoseconds;
}timestamp; 
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=1)> Public Structure timestamp
   Dim seconds_msb As UInt16
   Dim seconds_lsb As UInt32
   Dim nanoseconds As UInt32
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=1)]
public struct timestamp
{
   public UInt16 seconds_msb;
   public UInt32 seconds_lsb;
   public UInt32 nanoseconds;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item         | Description                                                              |
| ------------ | ------------------------------------------------------------------------ |
| seconds\_msb | Most significant portion of Integer value of the time stamp in seconds.  |
| seconds\_lsb | Least significant portion of Integer value of the time stamp in seconds. |
| nanoseconds  | Fractional seconds in nanoseconds                                        |
