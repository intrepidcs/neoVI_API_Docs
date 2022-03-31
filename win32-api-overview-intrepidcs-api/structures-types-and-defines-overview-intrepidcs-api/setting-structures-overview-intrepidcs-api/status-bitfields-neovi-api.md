# Status Bitfields - neoVI API

There are two status bitfields in the [message structures](message-structures-neovi-api.md) that define specific attributes of the message. The two status bitfields are named StatusBitfield and StatusBitfield1.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
const long SPY_STATUS_GLOBAL_ERR = 0x01;
const long SPY_STATUS_TX_MSG = 0x02;
const long SPY_STATUS_XTD_FRAME = 0x04;
const long SPY_STATUS_REMOTE_FRAME = 0x08;

const long SPY_STATUS_CRC_ERROR = 0x10;
const long SPY_STATUS_CAN_ERROR_PASSIVE = 0x20;
const long SPY_STATUS_INCOMPLETE_FRAME = 0x40;
const long SPY_STATUS_LOST_ARBITRATION = 0x80;

const long SPY_STATUS_UNDEFINED_ERROR = 0x100;
const long SPY_STATUS_CAN_BUS_OFF = 0x200;
const long SPY_STATUS_CAN_ERROR_WARNING = 0x400;
const long SPY_STATUS_BUS_SHORTED_PLUS = 0x800;

const long SPY_STATUS_BUS_SHORTED_GND = 0x1000;
const long SPY_STATUS_CHECKSUM_ERROR = 0x2000;
const long SPY_STATUS_BAD_MESSAGE_BIT_TIME_ERROR = 0x4000;
const long SPY_STATUS_IFR_DATA = 0x8000;

const long SPY_STATUS_HARDWARE_COMM_ERROR = 0x10000;
const long SPY_STATUS_EXPECTED_LEN_ERROR = 0x20000;
const long SPY_STATUS_INCOMING_NO_MATCH = 0x40000;
const long SPY_STATUS_BREAK = 0x80000;

const long SPY_STATUS_AVSI_REC_OVERFLOW = 0x100000;
const long SPY_STATUS_TEST_TRIGGER = 0x200000;
const long SPY_STATUS_AUDIO_COMMENT = 0x400000;
const long SPY_STATUS_GPS_DATA = 0x800000;

const long SPY_STATUS_ANALOG_DIGITAL_INPUT = 0x1000000;
const long SPY_STATUS_TEXT_COMMENT = 0x2000000;
const long SPY_STATUS_NETWORK_MESSAGE_TYPE = 0x4000000;
const long SPY_STATUS_VSI_TX_UNDERRUN = 0x8000000;

const long SPY_STATUS_VSI_IFR_CRC_Bit = 0x10000000;
const long SPY_STATUS_INIT_MESSAGE = 0x20000000;
const long SPY_STATUS_HIGH_SPEED_MESSAGE = 0x40000000;
const long SPY_STATUS_FLEXRAY_SECOND_STARTUP_FRAME = 0x40000000;
const long SPY_STATUS_EXTENDED = 0x80000000;


// The second status bitfield
const long SPY_STATUS2_HAS_VALUE = 1;
const long SPY_STATUS2_VALUE_IS_BOOLEAN = 2;
const long SPY_STATUS2_HIGH_VOLTAGE = 4;
const long SPY_STATUS2_LONG_MESSAGE = 8;
const long SPY_STATUS2_GLOBAL_CHANGE = 0x10000;
const long SPY_STATUS2_ERROR_FRAME = 0x20000;
const long SPY_STATUS2_END_OF_LONG_MESSAGE = 0x100000;
const long SPY_STATUS2_LIN_ERR_RX_BREAK_NOT_0 = 0x200000;
const long SPY_STATUS2_LIN_ERR_RX_BREAK_TOO_SHORT = 0x400000;
const long SPY_STATUS2_LIN_ERR_RX_SYNC_NOT_55 = 0x800000;
const long SPY_STATUS2_LIN_ERR_RX_DATA_GREATER_8 = 0x1000000;
const long SPY_STATUS2_LIN_ERR_TX_RX_MISMATCH = 0x2000000;
const long SPY_STATUS2_LIN_ERR_MSG_ID_PARITY = 0x4000000;
const long SPY_STATUS2_ISO_FRAME_ERROR = 0x8000000;
const long SPY_STATUS2_LIN_SYNC_FRAME_ERROR = 0x8000000;
const long SPY_STATUS2_ISO_OVERFLOW_ERROR = 0x10000000;
const long SPY_STATUS2_LIN_ID_FRAME_ERROR = 0x10000000;
const long SPY_STATUS2_ISO_PARITY_ERROR = 0x20000000;
const long SPY_STATUS2_LIN_SLAVE_BYTE_ERROR = 0x20000000;
const long SPY_STATUS2_RX_TIMEOUT_ERROR = 0x40000000;
const long SPY_STATUS2_LIN_NO_SLAVE_DATA = 0x80000000;
const long SPY_STATUS2_MOST_PACKET_DATA = 0x200000;
const long SPY_STATUS2_MOST_STATUS = 0x400000;
const long PY_STATUS2_MOST_LOW_LEVEL = 0x800000;
const long SPY_STATUS2_MOST_CONTROL_DATA = 0x1000000;
const long SPY_STATUS2_MOST_MHP_USER_DATA = 0x2000000;
const long SPY_STATUS2_MOST_MHP_CONTROL_DATA = 0x4000000;
const long SPY_STATUS2_MOST_I2S_DUMP = 0x8000000;
const long SPY_STATUS2_MOST_TOO_SHORT = 0x10000000;
const long SPY_STATUS2_MOST_MOST50 = 0x20000000;
const long SPY_STATUS2_MOST_MOST150 = 0x40000000;
const long SPY_STATUS2_MOST_CHANGED_PAR = 0x80000000;
const long SPY_STATUS2_ETHERNET_CRC_ERROR = 0x200000;
const long SPY_STATUS2_ETHERNET_FRAME_TOO_SHORT = 0x400000;
const long SPY_STATUS2_ETHERNET_FCS_AVAILABLE = 0x800000;

// The third status bitfield
const long SPY_STATUS3_LIN_JUST_BREAK_SYNC = 1;
const long SPY_STATUS3_LIN_SLAVE_DATA_TOO_SHORT = 2;
const long SPY_STATUS3_LIN_ONLY_UPDATE_SLAVE_TABLE_ONCE = 4;
```
{% endtab %}

{% tab title="Visual Basic .NET Declares 1" %}
```vbnet
Public Enum icsSpyDataStatusBitfield
   icsSpyStatusGlobalError = 2 ^ 0
   icsSpyStatusTx = 2 ^ 1
   icsSpyStatusXtdFrame = 2 ^ 2
   icsSpyStatusRemoteFrame = 2 ^ 3
   icsSpyStatusErrCRCError = 2 ^ 4
   icsSpyStatusCANErrorPassive = 2 ^ 5
   icsSpyStatusErrIncompleteFrame = 2 ^ 6
   icsSpyStatusErrLostArbitration = 2 ^ 7
   icsSpyStatusErrUndefined = 2 ^ 8
   icsSpyStatusErrCANBusOff = 2 ^ 9
   icsSpyStatusErrCANErrorWarning = 2 ^ 10
   icsSpyStatusBusShortedPlus = 2 ^ 11
   icsSpyStatusBusShortedGnd = 2 ^ 12
   icsSpyStatusCheckSumError = 2 ^ 13
   icsSpyStatusErrBadMessageBitTimeError = 2 ^ 14
   icsSpyStatusIFRData = 2 ^ 15
   icsSpyStatusHardwareCommError = 2 ^ 16
   icsSpyStatusExpectedLengthError = 2 ^ 17
   icsSpyStatusIncomingNoMatch = 2 ^ 18
   icsSpyStatusBreak = 2 ^ 19
   icsSpyStatusAVT_VSIRecOverflow = 2 ^ 20
   icsSpyStatusTestTrigger = 2 ^ 21
   icsSpyStatusAudioCommentType = 2 ^ 22
   icsSpyStatusGPSDataValue = 2 ^ 23
   icsSpyStatusAnalogDigitalInputValue = 2 ^ 24
   icsSpyStatusTextCommentType = 2 ^ 25
   icsSpyStatusNetworkMessageType = 2 ^ 26
   icsSpyStatusVSI_TxUnderRun = 2 ^ 27
   icsSpyStatusVSI_IFR_CRCBit = 2 ^ 28
   icsSpyStatusInitMessage = 2 ^ 29
   icsSpyStatusHighSpeed = 2 ^ 30
   SPY_STATUS_FLEXRAY_SECOND_STARTUP_FRAME = 2 ^ 30
   SPY_STATUS_EXTENDED = 2 ^ 31
End Enum
```
{% endtab %}

{% tab title="Visual Basic .NET Declares 2" %}
```vbnet
Public Enum icsSpyDataStatusBitfield2
   SPY_STATUS2_HAS_VALUE = 1
   SPY_STATUS2_VALUE_IS_BOOLEAN = 2
   SPY_STATUS2_HIGH_VOLTAGE = 4
   SPY_STATUS2_LONG_MESSAGE = 8
   SPY_STATUS2_GLOBAL_CHANGE = &H10000
   SPY_STATUS2_ERROR_FRAME = &H20000
   SPY_STATUS2_END_OF_LONG_MESSAGE = &H100000
   SPY_STATUS2_LIN_ERR_RX_BREAK_NOT_0 = &H200000
   SPY_STATUS2_LIN_ERR_RX_BREAK_TOO_SHORT = &H400000
   SPY_STATUS2_LIN_ERR_RX_SYNC_NOT_55 = &H800000
   SPY_STATUS2_LIN_ERR_RX_DATA_GREATER_8 = &H1000000
   SPY_STATUS2_LIN_ERR_TX_RX_MISMATCH = &H2000000
   SPY_STATUS2_LIN_ERR_MSG_ID_PARITY = &H4000000
   SPY_STATUS2_ISO_FRAME_ERROR = &H8000000
   SPY_STATUS2_LIN_SYNC_FRAME_ERROR = &H8000000
   SPY_STATUS2_ISO_OVERFLOW_ERROR = &H10000000
   SPY_STATUS2_LIN_ID_FRAME_ERROR = &H10000000
   SPY_STATUS2_ISO_PARITY_ERROR = &H20000000
   SPY_STATUS2_LIN_SLAVE_BYTE_ERROR = &H20000000
   SPY_STATUS2_RX_TIMEOUT_ERROR = &H40000000
   SPY_STATUS2_LIN_NO_SLAVE_DATA = &H80000000
   SPY_STATUS2_MOST_PACKET_DATA = &H200000
   SPY_STATUS2_MOST_STATUS = &H400000
   PY_STATUS2_MOST_LOW_LEVEL = &H800000
   SPY_STATUS2_MOST_CONTROL_DATA = &H1000000
   SPY_STATUS2_MOST_MHP_USER_DATA = &H2000000
   SPY_STATUS2_MOST_MHP_CONTROL_DATA = &H4000000
   SPY_STATUS2_MOST_I2S_DUMP = &H8000000
   SPY_STATUS2_MOST_TOO_SHORT = &H10000000
   SPY_STATUS2_MOST_MOST50 = &H20000000
   SPY_STATUS2_MOST_MOST150 = &H40000000
   SPY_STATUS2_MOST_CHANGED_PAR = &H80000000
   SPY_STATUS2_ETHERNET_CRC_ERROR = &H200000
   SPY_STATUS2_ETHERNET_FRAME_TOO_SHORT = &H400000
   SPY_STATUS2_ETHERNET_FCS_AVAILABLE = &H800000
End Enum
```
{% endtab %}

{% tab title="C# Declares 1" %}
```csharp
public enum eDATA_STATUS_BITFIELD_1
{
   SPY_STATUS_GLOBAL_ERR = 0x01,
   SPY_STATUS_TX_MSG = 0x02,
   SPY_STATUS_XTD_FRAME = 0x04,
   SPY_STATUS_REMOTE_FRAME = 0x08,
   SPY_STATUS_CRC_ERROR = 0x10,
   SPY_STATUS_CAN_ERROR_PASSIVE = 0x20,
   SPY_STATUS_INCOMPLETE_FRAME = 0x40,
   SPY_STATUS_LOST_ARBITRATION = 0x80,
   SPY_STATUS_UNDEFINED_ERROR = 0x100,
   SPY_STATUS_CAN_BUS_OFF = 0x200,
   SPY_STATUS_CAN_ERROR_WARNING = 0x400,
   SPY_STATUS_BUS_SHORTED_PLUS = 0x800,
   SPY_STATUS_BUS_SHORTED_GND = 0x1000,
   SPY_STATUS_CHECKSUM_ERROR = 0x2000,
   SPY_STATUS_BAD_MESSAGE_BIT_TIME_ERROR = 0x4000,
   SPY_STATUS_IFR_DATA = 0x8000,
   SPY_STATUS_HARDWARE_COMM_ERROR = 0x10000,
   SPY_STATUS_EXPECTED_LEN_ERROR = 0x20000,
   SPY_STATUS_INCOMING_NO_MATCH = 0x40000,
   SPY_STATUS_BREAK = 0x80000,
   SPY_STATUS_AVSI_REC_OVERFLOW = 0x100000,
   SPY_STATUS_TEST_TRIGGER = 0x200000,
   SPY_STATUS_AUDIO_COMMENT = 0x400000,
   SPY_STATUS_GPS_DATA = 0x800000,
   SPY_STATUS_ANALOG_DIGITAL_INPUT = 0x1000000,
   SPY_STATUS_TEXT_COMMENT = 0x2000000,
   SPY_STATUS_NETWORK_MESSAGE_TYPE = 0x4000000,
   SPY_STATUS_VSI_TX_UNDERRUN = 0x8000000,
   SPY_STATUS_VSI_IFR_CRC_Bit = 0x10000000,
   SPY_STATUS_INIT_MESSAGE = 0x20000000,
   SPY_STATUS_HIGH_SPEED_MESSAGE = 0x40000000,
}
```
{% endtab %}

{% tab title="C# Declares 2" %}
```csharp
public enum eDATA_STATUS_BITFIELD_2
{
   SPY_STATUS2_HAS_VALUE = 0,
   SPY_STATUS2_VALUE_IS_BOOLEAN = 2,
   SPY_STATUS2_HIGH_VOLTAGE = 4,
   SPY_STATUS2_LONG_MESSAGE = 8,
}
```
{% endtab %}
{% endtabs %}

**Remarks**

The tables below describe the bitfields.

**Table 1 - StatusBitfield Elements**

| C/C++ Name                                  | VB Name                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SPY\_STATUS\_GLOBAL\_ERR                    | icsSpyStatusGlobalError               | This is set if the message has any other error bits set.                                                                                                                                                                                                                                                                                                                                                                                                   |
| SPY\_STATUS\_TX\_MSG                        | icsSpyStatusTx                        | This is set if the message was transmitted by this device.                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_XTD\_FRAME                     | icsSpyStatusXtdFrame                  | This is set if the CAN message received or transmitted has an extended (29 bit) identifier.                                                                                                                                                                                                                                                                                                                                                                |
| SPY\_STATUS\_REMOTE\_FRAME                  | icsSpyStatusRemoteFrame               | This is set if the CAN message received or transmitted is a remote frame.                                                                                                                                                                                                                                                                                                                                                                                  |
| SPY\_STATUS\_CRC\_ERROR                     | icsSpyStatusErrCRCError               | This is set for J1850 VPW messages which do not have a proper CRC byte.                                                                                                                                                                                                                                                                                                                                                                                    |
| SPY\_STATUS\_CAN\_ERROR\_PASSIVE            | icsSpyStatusCANErrorPassive           | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_INCOMPLETE\_FRAME              | icsSpyStatusErrIncompleteFrame        | This is set for a J1850 VPW message which is received that ended on a non-byte boundary.                                                                                                                                                                                                                                                                                                                                                                   |
| SPY\_STATUS\_LOST\_ARBITRATION              | icsSpyStatusErrLostArbitration        | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_UNDEFINED\_ERROR               | icsSpyStatusErrUndefined              | This is an undefined error in the neoVI hardware                                                                                                                                                                                                                                                                                                                                                                                                           |
| SPY\_STATUS\_CAN\_BUS\_OFF                  | icsSpyStatusErrCANBusOff              | This is set when there is a change in error status of a MCP2510 CAN controller. The bitfield of the error status is stored in data byte 1 of the message structure. A description of this bitfield is included in this [`topic`](https://1088112144-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FabyA6gDDBQ0CNbxlveQb%2Fuploads%2FJ8qpeLJzJm1wvLyAAcvP%2F2510Bitfield.png?alt=media\&token=5140e476-0f20-477f-94b0-198d488671d3)`` |
| SPY\_STATUS\_CAN\_ERROR\_WARNING            | icsSpyStatusErrCANErrorWarning        | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_BUS\_SHORTED\_PLUS             | icsSpyStatusBusShortedPlus            | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_BUS\_SHORTED\_GND              | icsSpyStatusBusShortedGnd             | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_CHECKSUM\_ERROR                | icsSpyStatusCheckSumError             | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_BAD\_MESSAGE\_BIT\_TIME\_ERROR | icsSpyStatusErrBadMessageBitTimeError | This is set for J1850 VPW messages which do not meet the specified bit times for the SOF or bit signals.                                                                                                                                                                                                                                                                                                                                                   |
| SPY\_STATUS\_IFR\_DATA                      | icsSpyStatusIFRData                   | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_HARDWARE\_COMM\_ERROR          | icsSpyStatusHardwareCommError         | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_EXPECTED\_LEN\_ERROR           | icsSpyStatusExpectedLengthError       | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_INCOMING\_NO\_MATCH            | icsSpyStatusIncomingNoMatch           | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_BREAK                          | icsSpyStatusBreak                     | This is set if the J1850 VPW break symbol has been received or is to be transmitted.                                                                                                                                                                                                                                                                                                                                                                       |
| SPY\_STATUS\_AVSI\_REC\_OVERFLOW            | icsSpyStatusAVT\_VSIRecOverflow       | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_TEST\_TRIGGER                  | icsSpyStatusTestTrigger               | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_AUDIO\_COMMENT                 | icsSpyStatusAudioCommentType          | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_GPS\_DATA                      | icsSpyStatusGPSDataValue              | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_ANALOG\_DIGITAL\_INPUT         | icsSpyStatusAnalogDigitalInputValue   | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_TEXT\_COMMENT                  | icsSpyStatusTextCommentType           | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_NETWORK\_MESSAGE\_TYPE         | icsSpyStatusNetworkMessageType        | This is set for all messages received from a vehicle network.                                                                                                                                                                                                                                                                                                                                                                                              |
| SPY\_STATUS\_VSI\_TX\_UNDERRUN              | icsSpyStatusVSI\_TxUnderRun           | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_VSI\_IFR\_CRC\_Bit             | icsSpyStatusVSI\_IFR\_CRCBit          | Not used in the neoVI API.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SPY\_STATUS\_INIT\_MESSAGE                  | icsSpyStatusInitMessage               | This is set if the transmitted message should generate the ISO/Keyword2000 initialization waveform.                                                                                                                                                                                                                                                                                                                                                        |
| SPY\_STATUS\_HIGH\_SPEED\_MESSAGE           | icsSpyStatusHighSpeed                 | This is set if the transmitted message is transmitted in high speed mode.                                                                                                                                                                                                                                                                                                                                                                                  |

**Table 2 - StatusBitfield2 Elements**

| C/C++ Name                       | VB Name                    | Description                                                                        |
| -------------------------------- | -------------------------- | ---------------------------------------------------------------------------------- |
| SPY\_STATUS2\_HAS\_VALUE         | icsSpyStatusHasValue       | Not used in the neoVI API.                                                         |
| SPY\_STATUS2\_VALUE\_IS\_BOOLEAN | icsSpyStatusValueIsBoolean | Not used in the neoVI API.                                                         |
| SPY\_STATUS2\_HIGH\_VOLTAGE      | icsSpyStatusHighVoltage    | This is set if the transmitted message is transmitted in high voltage wakeup mode. |
| SPY\_STATUS2\_LONG\_MESSAGE      | icsSpyStatusLongMessage    | Not used in the neoVI API.                                                         |

VB Module: bas\_neoVI.bas

C/C++ Header: neovi.h

C/C++ Library File: icsneoVI.lib

DLL File: icsneoVI.dll

VB.Net Module: bas\_neoVI.vb

C# Class: icsNeoClass.cs\\

### **Examples**

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
Determining if we there's an error in the message (This is indicated by SPY_STATUS_GLOBAL_ERR bit set)

if (mMsg.StatusBitField & SPY_STATUS_GLOBAL_ERR)
{
 // This message has an error in it
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Determining if we transmitted a message (This is indicated by icsSpyStatusTx bit set)

If (Msg.StatusBitField And icsSpyDataStatusBitfield.icsSpyStatusTx) > 0 Then
        '// The message was transmitted by us
End If

Transmitting a CAN Extended ID Remote Frame

'// Load the message to be transmitted ArbID = FF extended remote frame with DLC=4
With stMessagesTx
    .ArbIDOrHeader = &HFF
    .NumberBytesData = 4
    .StatusBitField = icsSpyDataStatusBitfield.icsSpyStatusXtdFrame + icsSpyDataStatusBitfield.icsSpyStatusRemoteFrame
End With
lResult = icsneoTxMessages(m_hObject, stMessagesTx, NETID_HSCAN, 1)
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
Determining if we there's an error in the message (This is indicated by SPY_STATUS_GLOBAL_ERR bit set)

if (mMsg.StatusBitField & SPY_STATUS_GLOBAL_ERR)
{
  // This message has an error in it
}
```
{% endtab %}
{% endtabs %}
