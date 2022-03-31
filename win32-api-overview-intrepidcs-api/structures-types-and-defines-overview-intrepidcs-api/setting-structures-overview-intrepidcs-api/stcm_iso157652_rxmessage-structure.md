# stCM\_ISO157652\_RxMessage Structure

This structure is used by [icsneoISO15765\_ReceiveMessage](../../message-functions-overview-intrepidcs-api/iso15765-message-functions-overview-intrepidcs-api/iso15765\_receivemessage-method-intrepidcs-api.md)

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2)) _stCM_ISO157652_RxMessage
{
  unsigned short vs_netid;
  unsigned char padding;
  unsigned int id;
  unsigned int id_mask;
  unsigned int fc_id;
  unsigned char flowControlExtendedAddress;
  unsigned char extendedAddress;
  unsigned char blockSize;
  unsigned char stMin;
  unsigned short cf_timeout;
  union{
     struct
     {
       unsigned id_29_bit_enable:1;
       unsigned fc_id_29_bit_enable:1;
       unsigned ext_address_enable:1;
       unsigned fc_ext_address_enable:1;
       unsigned enableflowControlTransmission:1;
       unsigned PaddingEnable:1;
       unsigned iscanFD:1;
       unsigned isBRSEnabled:1;
     };
     unsigned int flags;
  unsigned char reserved[16];
}stCM_ISO157652_RxMessage;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare 1" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure stCM_ISO157652_RxMessage
  Dim vs_netid As UInt16
  Dim padding As Byte
  Dim id As UInt32
  Dim id_mask As UInt32
  Dim fc_id As UInt32
  Dim flowControlExtendedAddress As Byte
  Dim extendedAddress As Byte
  Dim blockSize As Byte
  Dim stMin As Byte
  Dim cf_timeout As UInt16
  Dim flags As UInt32
  Dim reserved0 As Byte
  Dim reserved1 As Byte
  Dim reserved2 As Byte
  Dim reserved3 As Byte
  Dim reserved4 As Byte
  Dim reserved5 As Byte
  Dim reserved6 As Byte
  Dim reserved7 As Byte
  Dim reserved8 As Byte
  Dim reserved9 As Byte
  Dim reserved10 As Byte
  Dim reserved11 As Byte
  Dim reserved12 As Byte
  Dim reserved13 As Byte
  Dim reserved14 As Byte
  Dim reserved15 As Byte
End Structure
```
{% endtab %}

{% tab title="Visual Basic .NET Declare 2" %}
```vbnet
Enum stCM_ISO157652_TxMessage_Flags
   id_29_bit_enable = 1
   fc_id_29_bit_enable = 2
   ext_address_enable = 4
   fc_ext_address_enable = 8
   enableflowControlTransmission = 16
   PaddingEnable = 32,
   iscanFD = 64
   isBRSEnabled = 128
End Enum
```
{% endtab %}

{% tab title="C# Declare 1" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct stCM_ISO157652_RxMessage
{
  public UInt16 vs_netid;
  public byte padding;
  public UInt32 id;
  public UInt32 id_mask;
  public UInt32 fc_id;
  public byte flowControlExtendedAddress;
  public byte extendedAddress;
  public byte blockSize;
  public byte stMin;
  public UInt16 cf_timeout;
  public UInt32 flags;
  public byte reserved0;
  public byte reserved1;
  public byte reserved2;
  public byte reserved3;
  public byte reserved4;
  public byte reserved5;
  public byte reserved6;
  public byte reserved7;
  public byte reserved8;
  public byte reserved9;
  public byte reserved10;
  public byte reserved11;
  public byte reserved12;
  public byte reserved13;
  public byte reserved14;
  public byte reserved15;
}
```
{% endtab %}

{% tab title="C# Declare 2" %}
```csharp
public enum stCM_ISO157652_TxMessage_Flags : int
{
   id_29_bit_enable = 1,
   fc_id_29_bit_enable = 2,
   ext_address_enable = 4,
   fc_ext_address_enable = 8,
   enableflowControlTransmission = 16,
   PaddingEnable = 32,
   iscanFD = 64,
   isBRSEnabled = 128,
}
```
{% endtab %}
{% endtabs %}

### Remarks

**Structure Elements**

| Item                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| vs\_netid                  | Network ID for the message                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| padding                    | Character used for padding to fill the rest of the last frame                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| id                         | ArbID of the message to look for                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| id\_mask                   | Settable Mask for incoming ID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| fc\_id                     | ArbID for the flow control frame to send                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| flowControlExtendedAddress | Byte used for the extended address in outgoing flow control message                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| extendedAddress            | Byte to be used for the extended address                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| blockSize                  | Number of frames to wait before sending another flow control frame                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| stMin                      | Seperation time to send for consecutive frames                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| cf\_timeout                | Timeout to wait for flow control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| flags                      | <p>Bit field containing flags for transaction</p><table data-header-hidden><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Flag</td><td>Value</td></tr><tr><td>id_29_bit_enable: Enables 29 bit ID for ID to look for</td><td>1</td></tr><tr><td>fc_id_29_bit_enable: Enables 29 bit ID for Flow Control message.</td><td>2</td></tr><tr><td>ext_address_enable: Enables extended addressing to look for in Rx message</td><td>4</td></tr><tr><td>fc_ext_address_enable: Enables using an extended addressing byte in Flow Control frame</td><td>8</td></tr><tr><td>enableFlowControlTransmission: Enables sending a flow control frame</td><td>16</td></tr><tr><td>paddingEnable: enables padding for outgoing flow control frame</td><td>32</td></tr><tr><td>iscanFD: Sets transaction as CAN FD</td><td>64</td></tr><tr><td>isBRSEnabled: Enables Baud Rate Switch for CAN FD</td><td>128</td></tr></tbody></table> |
| reserved 16 bytes          | Reserved                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
