# ISO9141\_KEYWORD2000\_\_INIT\_STEP Structure

This structure defines settings for the ISO9141 and Keyword 2000 initialization step on neoVI Fire devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef VS_MODIFIER struct
{
    icscm_uint16 time_500us;
    icscm_uint16 k;
    icscm_uint16 l;
}ISO9141_KEYWORD2000__INIT_STEP;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)>Public Structure ISO9141_KEYWORD2000__INIT_STEP
    Dim time_500us As Int16
    Dim k As Int16
    Dim l As Int16
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct ISO9141_KEYWORD2000__INIT_STEP
{
    public UInt16 time_500us;
    public UInt16 k;
    public UInt16 l;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                                       | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- |
| [icscm\_uint16](../intrepid-api-data-types.md) time\_500us | Number of 500µs Ticks for state to be set                  |
| [icscm\_uint16](../intrepid-api-data-types.md) k           | <p>Sets the state of the K line<br>Low = 0<br>High = 1</p> |
| [icscm\_uint16](../intrepid-api-data-types.md) l           | <p>Sets the State of the L line<br>Low = 0<br>High = 1</p> |
