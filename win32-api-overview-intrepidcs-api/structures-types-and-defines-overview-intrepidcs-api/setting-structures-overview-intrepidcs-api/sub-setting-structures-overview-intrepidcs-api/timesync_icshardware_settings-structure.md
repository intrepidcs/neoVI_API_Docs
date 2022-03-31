# TIMESYNC\_ICSHARDWARE\_SETTINGS Structure

**Structure defining the parameters for Time Sync**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint8_t MasterEnable;
   uint8_t SlaveEnable;
   uint8_t MasterNetwork;
   uint8_t SlaveNetwork;
}TIMESYNC_ICSHARDWARE_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure TIMESYNC_ICSHARDWARE_SETTINGS
   Dim MasterEnable As Byte
   Dim SlaveEnable As Byte
   Dim MasterNetwork As Byte
   Dim SlaveNetwork As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct TIMESYNC_ICSHARDWARE_SETTINGS
{
   public byte MasterEnable;
   public byte SlaveEnable;
   public byte MasterNetwork;
   public byte SlaveNetwork;
}
```
{% endtab %}
{% endtabs %}

#### Remarks

| Item          | Description |
| ------------- | ----------- |
| MasterEnable  | Not Defined |
| SlaveEnable   | Not Defined |
| MasterNetwork | Not Defined |
| SlaveNetwork  | Not Defined |

