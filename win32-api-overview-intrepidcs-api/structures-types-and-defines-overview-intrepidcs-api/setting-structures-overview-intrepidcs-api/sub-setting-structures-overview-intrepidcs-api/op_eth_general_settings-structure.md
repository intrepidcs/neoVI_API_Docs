# OP\_ETH\_GENERAL\_SETTINGS Structure

Structure defining the parameter in OP\_ETH\_GENERAL\_SETTINGS

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
    uint8_t ucInterfaceType;
    uint8_t reserved0;
    uint8_t reserved1;
    uint8_t reserved2;
    uint16_t tapPair0;
    uint16_t tapPair1;
    uint16_t tapPair2;
    uint16_t tapPair3;
    uint16_t tapPair4;
    uint16_t tapPair5;
    uint32_t uFlags;
}OP_ETH_GENERAL_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure OP_ETH_GENERAL_SETTINGS
    Dim ucInterfaceType As Byte
    Dim reserved0 As Byte
    Dim reserved1 As Byte
    Dim reserved2 As Byte
    Dim tapPair0 As UInt16
    Dim tapPair1 As UInt16
    Dim tapPair2 As UInt16
    Dim tapPair3 As UInt16
    Dim tapPair4 As UInt16
    Dim tapPair5 As UInt16
    Dim uFlags As UInt32
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct OP_ETH_GENERAL_SETTINGS
{
    public byte ucInterfaceType;
    public byte reserved0;
    public byte reserved1;
    public byte reserved2;
    public UInt16 tapPair0;
    public UInt16 tapPair1;
    public UInt16 tapPair2;
    public UInt16 tapPair3;
    public UInt16 tapPair4;
    public UInt16 tapPair5;
    public UInt32 uFlags;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item            | Description                                                                         |
| --------------- | ----------------------------------------------------------------------------------- |
| ucInterfaceType | <p>Sets the mode of the device</p><p>0=Tap 1= Media Converter 2=Low Latency Tab</p> |
| reserved0       | Reserved                                                                            |
| reserved1       | Reserved                                                                            |
| reserved2       | Reserved                                                                            |
| tapPair0        | For future use                                                                      |
| tapPair1        | For future use                                                                      |
| tapPair2        | For future use                                                                      |
| tapPair3        | For future use                                                                      |
| tapPair4        | For future use                                                                      |
| tapPair5        | For future use                                                                      |
| uFlags          | Reserved                                                                            |
