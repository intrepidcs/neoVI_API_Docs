# GPTPStatus Structure

This structure defines settings for the GPTPStatus structure.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(1))
{
   timestamp current_time;
   priority_vector gm_priority;
   int64_t ms_offset_ns;
   uint8_t is_sync;
   uint8_t link_status;
   int64_t link_delay_ns;
   uint8_t selected_role;
   uint8_t as_capable;
   uint8_t is_syntonized;
   uint8_t Reserved0;
   uint8_t Reserved1;
   uint8_t Reserved2;
   uint8_t Reserved3;
   uint8_t Reserved4;
   uint8_t Reserved5;
   uint8_t Reserved6;
   uint8_t Reserved7;
}GPTPStatus;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=1)> Public Structure GPTPStatus
   Dim current_time As timestamp
   Dim gm_priority As priority_vector
   Dim ms_offset_ns As Int64
   Dim is_sync As Byte
   Dim link_status As Byte
   Dim link_delay_ns As Int64
   Dim selected_role As Byte
   Dim as_capable As Byte
   Dim is_syntonized As Byte
   Dim Reserved0 As Byte
   Dim Reserved1 As Byte
   Dim Reserved2 As Byte
   Dim Reserved3 As Byte
   Dim Reserved4 As Byte
   Dim Reserved5 As Byte
   Dim Reserved6 As Byte
   Dim Reserved7 As Byte
End Structure 
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=1)]
public struct GPTPStatus
{
   public timestamp current_time;
   public priority_vector gm_priority;
   public Int64 ms_offset_ns;
   public byte is_sync;
   public byte link_status;
   public Int64 link_delay_ns;
   public byte selected_role;
   public byte as_capable;
   public byte is_syntonized;
   public byte Reserved0;
   public byte Reserved1;
   public byte Reserved2;
   public byte Reserved3;
   public byte Reserved4;
   public byte Reserved5;
   public byte Reserved6;
   public byte Reserved7;
}

```
{% endtab %}
{% endtabs %}

**Remarks**

| Item            | Description                                                                                                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| current\_time   | See timestamp structure                                                                                                                                                                                |
| gm\_priority    | See priority\_vector structure                                                                                                                                                                         |
| ms\_offset\_ns  | <p>Master slave offset in nano seconds<br>Valid when the port role is in slave mode.</p>                                                                                                               |
| is\_sync        | <p>Returns the gptp is synchronization status.<br>un-synced = 0<br>synced = 1<br>- valid when the port role is in slave mode.</p>                                                                      |
| link\_status    | <p>Gives the link status of the gptp enabled port.<br>link down = 0<br>link up = 1</p>                                                                                                                 |
| link\_delay\_ns | <p>Gives the link delay between the device and the link partner in nano second. Value is valid when the device is<br>- in standard profile<br>- in automotive profile<br>- port role is slave mode</p> |
| selected\_role  | <p>Indicates current port role, disabled, master, slave or passive.<br>DISABLED = 0<br>PASSIVE = 1 (Passive is only available for gptp switch mode)<br>MASTER = 2<br>SLAVE = 3<br></p>                 |
| as\_capable     | <p>indicates 802.1AS capability<br>0 = Not 802.1AS capability<br>1 = 802.1AS capability</p>                                                                                                            |
| is\_syntonized  | Indicates if gPTP is syntonized or not. Valid when the port role is in slave mode. 1 = if device is syntonized with grand master 0 = if not                                                            |
| Reserved0       | Reserved                                                                                                                                                                                               |
| Reserved1       | Reserved                                                                                                                                                                                               |
| Reserved2       | Reserved                                                                                                                                                                                               |
| Reserved3       | Reserved                                                                                                                                                                                               |
| Reserved4       | Reserved                                                                                                                                                                                               |
| Reserved5       | Reserved                                                                                                                                                                                               |
| Reserved6       | Reserved                                                                                                                                                                                               |
| Reserved7       | Reserved                                                                                                                                                                                               |
