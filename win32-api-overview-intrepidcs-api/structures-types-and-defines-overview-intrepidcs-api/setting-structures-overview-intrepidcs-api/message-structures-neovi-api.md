# Message Structures - neoVI API

These structures are used to represent messages both received and transmitted by the neoVI device. These structures can also be represented as an [array of bytes described in a separate topic](using-an-array-instead-of-a-message-structure-intrepidcs-api.md).

{% tabs %}
{% tab title="C/C++ Declare 1" %}
```cpp
typedef struct // matching C structure
{
    unsigned long StatusBitField;
    unsigned long StatusBitField2;
    unsigned long TimeHardware;
    unsigned long TimeHardware2;
    unsigned long TimeSystem;
    unsigned long TimeSystem2;
    unsigned char TimeStampHardwareID;
    unsigned char TimeStampSystemID;
    unsigned char NetworkID;
    unsigned char NodeID;
    unsigned char Protocol;
    unsigned char MessagePieceID;
    unsigned char ExtraDataPtrEnabled;
    unsigned char NumberBytesHeader;
    unsigned char NumberBytesData;
    unsigned char NetworkID2;
    short DescriptionID;
    long ArbIDOrHeader;
    unsigned char Data[8];
    unsigned long StatusBitField3;
    unsigned long StatusBitField4;
    void * ExtraDataPtr;
    unsigned char MiscData;
    char Reserved[3];
} icsSpyMessage;
```
{% endtab %}

{% tab title="C/C++ Declare 2" %}
```cpp
typedef struct // matching C structure
{
    unsigned long StatusBitField;
    unsigned long StatusBitField2;
    unsigned long TimeHardware;
    unsigned long TimeHardware2;
    unsigned long TimeSystem;
    unsigned long TimeSystem2;
    unsigned char TimeStampHardwareID;
    unsigned char TimeStampSystemID;
    unsigned char NetworkID;
    unsigned char NodeID;
    unsigned char Protocol;
    unsigned char MessagePieceID;
    unsigned char ExtraDataPtrEnabled;
    unsigned char NumberBytesHeader;
    unsigned char NumberBytesData;
    unsigned char NetworkID2;
    short DescriptionID;
    unsigned char Header[4];
    unsigned char Data[8];
    unsigned long StatusBitField3;
    unsigned long StatusBitField4;
    void * ExtraDataPtr;
    unsigned char MiscData;
    char Reserved[3];
} icsSpyMessageJ1850;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares 1" %}
```vbnet
Public Structure icsSpyMessage
    Dim StatusBitField As Int32
    Dim StatusBitField2 As Int32
    Dim TimeHardware As UInt32
    Dim TimeHardware2 As UInt32
    Dim TimeSystem As UInt32
    Dim TimeSystem2 As UInt32
    Dim TimeStampHardwareID As Byte
    Dim TimeStampSystemID As Byte
    Dim NetworkID As Byte
    Dim NodeID As Byte
    Dim Protocol As Byte
    Dim MessagePieceID As Byte
    Dim ExtraDataPtrEnabled As Byte
    Dim NumberBytesHeader As Byte
    Dim NumberBytesData As Byte
    Dim NetworkID2 As Byte
    Dim DescriptionID As Int16
    Dim ArbIDOrHeader As Int32
    Dim Data1 As Byte
    Dim Data2 As Byte
    Dim Data3 As Byte
    Dim Data4 As Byte
    Dim Data5 As Byte
    Dim Data6 As Byte
    Dim Data7 As Byte
    Dim Data8 As Byte
    Dim StatusBitField3 As Int32
    Dim StatusBitField4 As Int32
    Dim iExtraDataPtr As IntPtr
    Dim MiscData As Byte
    Dim Reserved0 as Byte
    Dim Reserved1 as Byte
    Dim Reserved2 as Byte
End Structure
```
{% endtab %}

{% tab title="Visual Basic .NET Declares 2" %}
```vbnet
Public Structure icsSpyMessageJ1850
    Dim StatusBitField As Int32
    Dim StatusBitField2 As Int32
    Dim TimeHardware As UInt32
    Dim TimeHardware2 As UInt32
    Dim TimeSystem As UInt32
    Dim TimeSystem2 As UInt32
    Dim TimeStampHardwareID As Byte
    Dim TimeStampSystemID As Byte
    Dim NetworkID As Byte
    Dim NodeID As Byte
    Dim Protocol As Byte
    Dim MessagePieceID As Byte
    Dim ExtraDataPtrEnabled As Byte
    Dim NumberBytesHeader As Byte
    Dim NumberBytesData As Byte
    Dim NetworkID2 as Byte
    Dim DescriptionID As Int16
    Dim Header1 As Byte
    Dim Header2 As Byte
    Dim Header3 As Byte
    Dim Header4 As Byte
    Dim Data1 As Byte
    Dim Data2 As Byte
    Dim Data3 As Byte
    Dim Data4 As Byte
    Dim Data5 As Byte
    Dim Data6 As Byte
    Dim Data7 As Byte
    Dim Data8 As Byte
    Dim StatusBitField3 As Int32
    Dim StatusBitField4 As Int32
    Dim iExtraDataPtr As IntPtr
    Dim MiscData As Byte
    Dim Reserved0 as Byte
    Dim Reserved1 as Byte
    Dim Reserved2 as Byte
End Structure
```
{% endtab %}

{% tab title="C# Declares 1" %}
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct icsSpyMessage
{
    public int StatusBitField;
    public int StatusBitField2;
    public int TimeHardware;
    public int TimeHardware2;
    public int TimeSystem;
    public int TimeSystem2;
    public byte TimeStampHardwareID;
    public byte TimeStampSystemID;
    public byte NetworkID;
    public byte NodeID;
    public byte Protocol;
    public byte MessagePieceID;
    public byte ExtraDataPtrEnabled;
    public byte NumberBytesHeader;
    public byte NumberBytesData;
    public byte NetworkID2;
    public short DescriptionID;
    public int ArbIDOrHeader;
    public byte Data1;
    public byte Data2;
    public byte Data3;
    public byte Data4;
    public byte Data5;
    public byte Data6;
    public byte Data7;
    public byte Data8;
    public int StatusBitField3;
    public int StatusBitField4;
    public IntPtr iExtraDataPtr;
    public byte MiscData;
    public byte Reserved0;
    public byte Reserved1;
    public byte Reserved2;
}
```
{% endtab %}

{% tab title="C# Declares 2" %}
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct icsSpyMessageJ1850
{
    public int StatusBitField;
    public int StatusBitField2;
    public int TimeHardware;
    public int TimeHardware2;
    public int TimeSystem;
    public int TimeSystem2;
    public byte TimeStampHardwareID;
    public byte TimeStampSystemID;
    public byte NetworkID;
    public byte NodeID;
    public byte Protocol;
    public byte MessagePieceID;
    public byte ExtraDataPtrEnabled;
    public byte NumberBytesHeader;
    public byte NumberBytesData;
    public byte NetworkID2;
    public short DescriptionID;
    public byte Header1;
    public byte Header2;
    public byte Header3;
    public byte Header4;
    public byte Data1;
    public byte Data2;
    public byte Data3;
    public byte Data4;
    public byte Data5;
    public byte Data6;
    public byte Data7;
    public byte Data8;
    public int StatusBitField3;
    public int StatusBitField4;
    public IntPtr iExtraDataPtr;
    public byte MiscData;
    public byte Reserved0;
    public byte Reserved1;
    public byte Reserved2;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

There are two structures here. Both are equivalent. The only difference is how they represent message bytes. The icsspyMessageJ1850 provides a more convenient representation for J1850 or ISO messages with a header array holding the first three bytes of the message.

These structures can be use interchangeably in C by casting one type to the other. In Visual Basic, you can copy one structure to the other using the LSet method.

Table 1 below lists the members of the structure and specific remarks about there use.

**Table 1 - Message Structure Elements**

| Item                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| StatusBitField StatusBitField2 StatusBitField3 StatusBitField4 | Bitfields which describe the message. These are described in a [separate topic](status-bitfields-neovi-api.md).                                                                                                                                                                                                                                                                                          |
| TimeHardware TimeHardware2                                     | This is the hardware time stamp. The function [GetTimeStampForMsg](../../message-functions-overview-intrepidcs-api/gettimestampformsg-method-intrepidcs-api.md) will convert these to seconds. If the hardware has an RTC (Real Time Clock), T-0 is Jan 1, 2007. Other devices start when the unit is powered or connected to by open function.                                                          |
| TimeSystem TimeSystem2                                         | This is the system time stamp. TimeSystem is loaded with the value received from the timeGetTime call in the WIN32 multimedia API. The timeGetTime accuracy is up to 1 millisecond. See the WIN32 API documentation for more information. This timestamp is useful for time comparing with other system events or data which is not synced with the neoVI timestamp. Currently, TimeSystem2 is not used. |
| TimeStampHardwareID                                            | This is an identifier of what type of hardware timestamp is used. Since neoVI’s timestamp is always the same, this doesn’t change.                                                                                                                                                                                                                                                                       |
| TimeStampSystemID                                              | This is an identifier of what type of system timestamp is used. Since WIN32 neoVI’s timestamp is always the same, from the timeGetTime API, this doesn’t change.                                                                                                                                                                                                                                         |
| NetworkID NetworkID2                                           | This is the NetworkID as assigned in the OpenPort method. This value is used to identify which network this message was received on. The topic here [NetworkIDList](neovi-network-id-list.md) contains the ID mapping NetworkID2 is a continuation. NetworkID + (NetworkID2 \* 100) can be used to join this into one value.                                                                             |
| NodeID                                                         | Not Used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                               |
| Protocol                                                       | This is the type of protocol which the message belongs to. Valid values are SPY\_PROTOCOL\_CAN, SPY\_PROTOCOL\_CANFD, and SPY\_PROTOCOL\_ISO9141.                                                                                                                                                                                                                                                        |
| MessagePieceID                                                 | Not Used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                               |
| ExtraDataPtrEnabled                                            | Flag indicating if the data section (when set to 0) is used or the data at the pointer location of iExtraDataPtr (when set to 1).                                                                                                                                                                                                                                                                        |
| NumberBytesHeader                                              | Used for J1850/ISO messages. It indicates how many bytes are stored in the Header(1 to 4) array.                                                                                                                                                                                                                                                                                                         |
| NumberBytesData                                                | Holds the number of bytes in the Data(1 to 8) array or the number of bytes in a CAN remote frame (The DLC).                                                                                                                                                                                                                                                                                              |
| DescriptionID                                                  | Not Used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                               |
| Header(1 To 4) or ArbIDOrHeader                                | Holds up to 3 byte 1850 header (bytes 1 through 3) or a 29 bit CAN header.                                                                                                                                                                                                                                                                                                                               |
| Data(1 To 8)                                                   | Holds the 8 data bytes in CAN messages or bytes 4 through 11 in J1850/ISO messages.                                                                                                                                                                                                                                                                                                                      |
| iExtraDataPtr                                                  | Pointer to data bytes for CAN FD and Ethernet messages containing over 8 bytes. ExtraDataPtrEnabled must be 1 to use this.                                                                                                                                                                                                                                                                               |
| MiscData                                                       | Not Used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                               |

### **Examples**

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
Interchangeably using the structures : Casting a icsSpyMessage to an icsSpyMessageJ1850

((icsSpyMessageJ1850 *) stMessages)[lCount].Header[0]

Timestamps : Calculating a TimeStamp

// Calculate the time for this message
dTime = ((double) stMessages[lCount].TimeHardware2) * NEOVI_TIMESTAMP_2 + 
                ((double) stMessages[lCount].TimeHardware) * NEOVI_TIMESTAMP_1;
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
Timestamps : Calculating a TimeStamp

double dTime; //Storage for message time

dTime = icsNeoDll.icsneoGetTimeStamp(stMessages[lCount-1].TimeHardware, stMessages[lCount-1].TimeHardware2);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Timestamps : Calculating a TimeStamp

Dim dTime As Double

dTime = icsneoGetTimeStamp(stMessages(lCount - 1).TimeHardware, stMessages(lCount - 1).TimeHardware2)
```
{% endtab %}
{% endtabs %}
