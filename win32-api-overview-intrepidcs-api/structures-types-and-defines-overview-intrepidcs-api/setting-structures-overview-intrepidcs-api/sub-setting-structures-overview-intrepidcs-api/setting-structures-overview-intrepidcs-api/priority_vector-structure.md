# priority\_vector Structure

This structure defines settings for the priority\_Vector structure for gPTP.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(1))
{
   system_identity sysid;
   uint16_t steps_removed;
   port_identity portid;
   uint16_t port_number;
}priority_vector; 
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=1)> Public Structure priority_vector
   Dim sysid As system_identity
   Dim steps_removed As UInt16
   Dim portid As port_identity
   Dim port_number As UInt16
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=1)]
public struct priority_vector
{
   public system_identity sysid;
   public UInt16 steps_removed;
   public port_identity portid;
   public UInt16 port_number;
}

```
{% endtab %}
{% endtabs %}

**Remarks**

| Item           | Description                                                       |
| -------------- | ----------------------------------------------------------------- |
| sysid          | See system\_identity structure                                    |
| steps\_removed | Indicates the number of Network paths from the root the source is |
| portid         | See port\_identity structure                                      |
| port\_number   | portNumber represents the PTP ports on the network.               |
