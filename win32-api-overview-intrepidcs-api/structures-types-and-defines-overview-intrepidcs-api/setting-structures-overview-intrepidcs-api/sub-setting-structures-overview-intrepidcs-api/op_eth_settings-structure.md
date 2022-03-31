# OP\_ETH\_SETTINGS Structure

This structure defines various settings for OP BR Ethernet networks.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
    unsigned char ucConfigMode;
    unsigned char preemption_en;
    unsigned char mac_addr1_0;
    unsigned char mac_addr1_1;
    unsigned char mac_addr1_2;
    unsigned char mac_addr1_3;
    unsigned char mac_addr1_4;
    unsigned char mac_addr1_5;
    unsigned char mac_addr2_0;
    unsigned char mac_addr2_1;
    unsigned char mac_addr2_2;
    unsigned char mac_addr2_3;
    unsigned char mac_addr2_4;
    unsigned char mac_addr2_5;
    unsigned char OpEthFlags;
    unsigned char Reserved;
}OP_ETH_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure OP_ETH_SETTINGS
    Dim ucConfigMode As Byte
    Dim preemption_en As Byte
    Dim mac_addr1_0 As Byte
    Dim mac_addr1_1 As Byte
    Dim mac_addr1_2 As Byte
    Dim mac_addr1_3 As Byte
    Dim mac_addr1_4 As Byte
    Dim mac_addr1_5 As Byte
    Dim mac_addr2_0 As Byte
    Dim mac_addr2_1 As Byte
    Dim mac_addr2_2 As Byte
    Dim mac_addr2_3 As Byte
    Dim mac_addr2_4 As Byte
    Dim mac_addr2_5 As Byte
    Dim OpEthFlags As Byte
    Dim Reserved As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct OP_ETH_SETTINGS
{
    public byte ucConfigMode;
    public byte preemption_en;
    public byte mac_addr1_0;
    public byte mac_addr1_1;
    public byte mac_addr1_2;
    public byte mac_addr1_3;
    public byte mac_addr1_4;
    public byte mac_addr1_5;
    public byte mac_addr2_0;
    public byte mac_addr2_1;
    public byte mac_addr2_2;
    public byte mac_addr2_3;
    public byte mac_addr2_4;
    public byte mac_addr2_5;
    public byte OpEthFlags;
    public byte Reserved;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ucConfigMode   | Sets the Link Mode. 0=Auto: 1=Master: 2=Slave                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| preemption\_en | Enables Preemption Support (IEEE802.3Br). 0=Disabled: 1=Enabled                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| mac\_addr1\_0  | First byte of Original MAC address XX:11:22:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| mac\_addr1\_1  | Second byte of Original MAC address 00:XX:22:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| mac\_addr1\_2  | Third byte of Original MAC address 00:11:XX:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| mac\_addr1\_3  | Fourth byte of Original MAC address 00:11:22:XX:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| mac\_addr1\_4  | Fifth byte of Original MAC address 00:11:22:33:XX:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| mac\_addr1\_5  | Sixth First byte of Original MAC address 00:11:22:33:44:XX                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| mac\_addr2\_0  | First byte of Spoof MAC address XX:11:22:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| mac\_addr2\_1  | Second byte of Spoof MAC address 00:XX:22:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| mac\_addr2\_2  | Third byte of Spoof MAC address 00:11:XX:33:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| mac\_addr2\_3  | fourth byte of Spoof MAC address 00:11:22:XX:44:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| mac\_addr2\_4  | Fifth byte of Spoof MAC address 00:11:22:33:XX:55                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| mac\_addr2\_5  | Sixth byte of Spoof MAC address 00:11:22:33:44:XX                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| OpEthFlags     | <p>Bitfield of options</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Item: Location</td><td>Function</td></tr><tr><td>mac_spoofing_en: Bit 0</td><td>State of enabling Mac Spoofing. 0=No Spoofing: 1=Spoof</td></tr><tr><td>mac_spoofing_isDstOrSrc: Bit 1</td><td>Spoof source or Destination 0=Destination: 1=Source</td></tr><tr><td>Link_Spd_A: Bit 2 Link_Spd_B: Bit 3</td><td>Sets Link Speed 0 0 = 10Mbps 0 1 = 100Mbps 1 0 = 1000Mbps</td></tr><tr><td>Q2112_Phy_Mode: Bit 4</td><td>Sets Phy Mode 0=IEEE: 1=Legacy</td></tr></tbody></table> |
| Reserved       | Not Available                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
