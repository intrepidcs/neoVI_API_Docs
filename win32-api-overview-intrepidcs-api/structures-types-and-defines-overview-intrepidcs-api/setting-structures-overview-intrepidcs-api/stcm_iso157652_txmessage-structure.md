# stCM\_ISO157652\_TxMessage Structure

This structure is used by [icsneoISO15765\_TransmitMessage](../../message-functions-overview-intrepidcs-api/iso15765-message-functions-overview-intrepidcs-api/iso15765\_transmitmessage-method-intrepidcs-api.md)

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec(align(2)) _stCM_ISO157652_TxMessage
{
    unsigned short vs_netid; 
    unsigned char padding; 
    unsigned char reserved2;
    unsigned int id; 
    unsigned int fc_id; 
    unsigned int fc_id_mask; 
    unsigned char stMin;
    unsigned char blockSize;
    unsigned char flowControlExtendedAddress; 
    unsigned char extendedAddress; 

    unsigned short fs_timeout; 
    unsigned short fs_wait; 
   
    unsigned char data[4*1024]; 
    unsigned int num_bytes;
    union
    { 
        struct
        {
            unsigned id_29_bit_enable:1; 
            unsigned fc_id_29_bit_enable:1; 
            unsigned ext_address_enable:1; 
            unsigned fc_ext_address_enable:1; 
            unsigned overrideSTmin:1;
            unsigned overrideBlockSize:1;
            unsigned paddingEnable:1;
            unsigned iscanFD : 1;
            unsigned isBRSEnabled : 1;        };
    unsigned short flags;
};
```
{% endtab %}

{% tab title="Visual Basic .NET Declare 1" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure stCM_ISO157652_TxMessage
    Dim vs_netid As UInt16
    Dim padding As Byte
    Dim reserved2 As Byte
    Dim id As UInt32
    Dim fc_id As UInt32
    Dim fc_id_mask As UInt32
    Dim stMin As Byte
    Dim blockSize As Byte
    Dim flowControlExtendedAddress As Byte 
    Dim extendedAddress As Byte
    '//flow control timeouts
    Dim fs_timeout As UInt16
    Dim fs_wait As UInt16
    '//******************************************************************************************************************
    <VBFixedArray(4095), System.Runtime.InteropServices.MarshalAs(System.Runtime.InteropServices.UnmanagedType.ByValArray, SizeConst:=4095)> Public data() As Byte
    '// call: stCM_ISO157652_TxMessage.data = New Byte(4096) {}
    '//******************************************************************************************************************
    Dim num_bytes As UInt32
    Dim flags As UInt16
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
    overrideSTmin = 16 
    overrideBlockSize = 32 
    paddingEnable = 64 
    iscanFD = 128 
    isBRSEnabled= 256
End Enum
```
{% endtab %}

{% tab title="C# Declare 1" %}
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 2)]
public struct {
    public UInt16 vs_netid;
    public byte padding;
    public bytete reserved2;
    public id;
    public UInt32 fc_id; 
    public UInt3232
    public bytete
    public byte blockSize;
    public bytete
    public bytete
    public UInt16 fs_timeout;
    public UInt16 fs_wait; 
    //******************************************************************************************************************
    [MarshalAs(>(UnmanagedType.ByValArray,SizeConst=4095)] public byte[] data;
    // call: stCM_ISO157652_TxMessage.data = new byte(4096)
    //******************************************************************************************************************
    public num_bytes;
    public UInt16 flags;
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
    overrideSTmin = 16, 
    overrideBlockSize = 32, 
    paddingEnable = 64, 
    iscanFD = 128,
    isBRSEnabled= 256,
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| unsigned short vs\_netID                 | Network ID of the message                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| unsigned char padding                    | Character used for padding to fill the rest of the last frame.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| unsigned char reserved2                  | Reserved set to 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| unsigned int id                          | ArbID of the message being sent                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| unsigned int fc\_id                      | ArbID of the flow control frame to look for                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| unsigned int fc\_id\_mask                | Bitwise mask for the flow control arbitration ID. (1 pass 0 block)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| unsigned char stMin                      | Separation time to wait between consecutive frames                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| unsigned char blockSize                  | Number of consecutive frames before expecting another flow control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| unsigned char flowControlExtendedAddress | Byte used expected for flow control extended address when using extended addressing (different than 29bit IDs)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| unsigned char extendedAddress            | Byte used for extended address in transmitted message                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| unsigned short fs\_timeout               | Timeout to wait for flow control frame                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| unsigned short fs\_wait                  | Timeout to wait for 7F 78 (Negative response of request received response pending                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| unsigned char \[4096]                    | Data array of 4096 that contains the data to send                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| unsigned int num\_bytes                  | Number of data bytes used in the data array                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| unsigned short flags                     | <p>Bit field containing flags for transaction</p><table><thead><tr><th>id_29_bit_enable</th><th>Enable 29 Bit</th><th>address 1</th></tr></thead><tbody><tr><td>fc_id_29_bit_enable</td><td>Flow control 29 bit address</td><td>2</td></tr><tr><td>ext_address_enable</td><td>Use extended address</td><td>4</td></tr><tr><td>fc_extended_address_enable</td><td>Flow Control use extended address</td><td>8</td></tr><tr><td>overrideSTmin</td><td>Ignore ST Min in flow control</td><td>16</td></tr><tr><td>overrideBlockSize</td><td>Ignore block size in flow control</td><td>32</td></tr><tr><td>paddingenable</td><td>Pad outgoing frames</td><td>64</td></tr><tr><td>iscanFD</td><td>Enables CAN FD</td><td>128</td></tr><tr><td>isBRSEnabled</td><td>Enables CAN FD Baud Rate Switch</td><td>256</td></tr></tbody></table> |
