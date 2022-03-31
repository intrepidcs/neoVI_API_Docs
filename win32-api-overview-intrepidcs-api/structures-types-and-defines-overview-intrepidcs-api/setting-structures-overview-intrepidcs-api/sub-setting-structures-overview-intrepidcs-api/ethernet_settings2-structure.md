# ETHERNET\_SETTINGS2 Structure

This structure defines various settings for Ethernet networks.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint8_t flags;
   uint8_t link_speed;
   uint32_t ip_addr;
   uint32_t netmask;
   uint32_t gateway;
   int16_t rsvd0;
}ETHERNET_SETTINGS2;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure ETHERNET_SETTINGS2
   Dim flags As Byte
   Dim link_speed As Byte
   Dim ip_addr As UInt32
   Dim netmask As UInt32
   Dim gateway As UInt32
   Dim rsvd0 As Int16
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct ETHERNET_SETTINGS2
{
   public byte flags;
   public byte link_speed;
   public UInt32 ip_addr;
   public UInt32 netmask;
   public UInt32 gateway;
   public Int16 rsvd0;
```
{% endtab %}
{% endtabs %}

#### **Remarks**

| Item        | Description                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| flags       | <table><thead><tr><th>Bit</th><th>Function</th></tr></thead><tbody><tr><td>Bit 0</td><td>0=half duplex, 1=full duplex</td></tr><tr><td>Bit 1</td><td>1=Enable Autonegotiation</td></tr><tr><td>Bit 2</td><td>1= Enable tcpip stack</td></tr><tr><td>Bit 3</td><td>1=Enable rtsp server</td></tr><tr><td>Bit 4</td><td>1=Enable ICS device hosting</td></tr><tr><td>Bit 5</td><td>1=Config not allowed</td></tr></tbody></table> |
| link\_speed | 0 = 10B, 1 = 100B, 2=1000B                                                                                                                                                                                                                                                                                                                                                                                                      |
| ip\_addr    | Not Defined                                                                                                                                                                                                                                                                                                                                                                                                                     |
| netmask     | Not Defined                                                                                                                                                                                                                                                                                                                                                                                                                     |
| gateway     | Not Defined                                                                                                                                                                                                                                                                                                                                                                                                                     |
| rsvd0       | Not Defined                                                                                                                                                                                                                                                                                                                                                                                                                     |
