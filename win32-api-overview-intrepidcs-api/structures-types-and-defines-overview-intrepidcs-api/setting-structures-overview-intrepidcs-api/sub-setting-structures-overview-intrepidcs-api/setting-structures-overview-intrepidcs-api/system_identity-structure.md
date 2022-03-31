# system\_identity Structure

This structure defines settings for system\_identity for gPTP

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(1))
{
   uint8_t priority_1;
   clock_quality clock_quality;
   uint8_t priority_2;
   uint64_t clock_identity;
}system_identity; 
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=1)> Public Structure system_identity
   Dim priority_1 As Byte
   Dim clock_quality As clock_quality
   Dim priority_2 As Byte
   Dim clock_identity As UInt64
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=1)]
public struct system_identity
{
   public byte priority_1;
   public clock_quality clock_quality;
   public byte priority_2;
   public UInt64 clock_identity;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item            | Description                                                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| priority\_1     | Priority1 sets the ordering priority. Lower values set a better ClockMaster. See gPTP spec, 8021AS for more details and restrictions. |
| clock\_quality  | See clock\_quality structure                                                                                                          |
| priority\_2     | priority2 uses a similar scheme as priority1. See gPTP spec, 8021AS for more details.                                                 |
| clock\_identity | clockIdentity attribute is defined in 7.5.2.2 of IEEE Std 1588-2019                                                                   |
