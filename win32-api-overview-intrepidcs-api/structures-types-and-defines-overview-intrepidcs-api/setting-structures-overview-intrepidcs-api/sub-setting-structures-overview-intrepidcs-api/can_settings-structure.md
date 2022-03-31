# CAN\_SETTINGS Structure

This structure defines settings for CAN networks on neoVI and ValueCAN devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
struct __declspec (align(2))
{
uint8_t Mode;
uint8_t SetBaudrate;
uint8_t Baudrate;
uint8_t transceiver_mode;
uint8_t TqSeg1;
uint8_t TqSeg2;
uint8_t TqProp;
uint8_t TqSync;
uint16_t BRP;
uint8_t auto_baud;
uint8_t innerFrameDelay25us;
}CAN_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure CAN_SETTINGS
    Dim Mode As Byte
    Dim SetBaudrate As Byte
    Dim Baudrate As Byte
    Dim transceiver_mode As Byte
    Dim TqSeg1 As Byte
    Dim TqSeg2 As Byte
    Dim TqProp As Byte
    Dim TqSync As Byte
    Dim BRP As UInt16
    Dim auto_baud As Byte
    Dim innerFrameDelay25us As Byte
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct CAN_SETTINGS
{
public byte Mode;
public byte SetBaudrate;
public byte Baudrate;
public byte transceiver_mode;
public byte TqSeg1;
public byte TqSeg2;
public byte TqProp;
public byte TqSync;
public UInt16 BRP;
public byte auto_baud;
public byte innerFrameDelay25us;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mode                | <p>Sets the mode of the CAN controller</p><p>Normal = 0 Disabled = 1 (neoVI FIRE/RED and ValueCAN3 only) Listen only = 3 Listen All = 7 (neoVI FIRE/RED and ValueCAN3 only)</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SetBaudrate         | <p>The bit rate of the CAN Channel can be selected in one of two ways. This sets the method to calculate the baud rate</p><p>Auto (Uses Bitrate parameter) = 0 Use TQ times = 1</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Baudrate            | <p>The bit rate of a CAN channel can be selected from a list of common bit rates Write the correct enumeration for the desired bit rate and ensure that SetBaudrate is 1(auto) Default value = 8</p><p>Note: This parameter is only applicable if SetBaudrate = 0</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>First Name</td><td>Last Name</td></tr><tr><td>20000</td><td>0</td></tr><tr><td>33333</td><td>1</td></tr><tr><td>50000</td><td>2</td></tr><tr><td>62500</td><td>3</td></tr><tr><td>83333</td><td>4</td></tr><tr><td>100000</td><td>5</td></tr><tr><td>125000</td><td>6</td></tr><tr><td>250000</td><td>7</td></tr><tr><td>500000</td><td>8</td></tr><tr><td>800000</td><td>9</td></tr><tr><td>1000000</td><td>10</td></tr></tbody></table> |
| transceiver\_mode   | Not used, set to 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| TqSeg1              | Phase segment 1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| TqSeg2              | Phase segment 2                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| TqProp              | Propagation delay                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| TqSync              | Syncro jump Width                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| BRP                 | Baud Rate Prescaler                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| auto\_baud          | Enabled Auto bitrate feature. (neoVI FIRE/RED and ValueCAN3) Enable = 1 Disable = 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| innerFrameDelay25us | Adjusts min time between frames (neoVI FIRE/RED and ValueCAN3 only)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
