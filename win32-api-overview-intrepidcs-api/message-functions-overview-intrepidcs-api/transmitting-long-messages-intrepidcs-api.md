# Transmitting Long Messages - Intrepidcs API

**Overview**

For ISO9141 and Keyword 2000 Networks, a long message transmission option is allowed. Long message transmission is necessary when the message length exceeds twelve bytes (including checksum if used).

You can transmit a long message by calling the [TxMessages](txmessages-method-intrepidcs-api.md) method with modified arguments. First, you will pass an array of icsSpyMessage structures which contain the long message data. This data in the array must be set properly. Finally, you must set the lNumMessages argument to the number of structures.

You must setup the long message data properly. For the first message, both the 3 byte Header and the 8 byte data section are filled in. For consecutive messages only the 8 byte data section is filled in.

**VB Example to Send a 16 byte message**

```vbnet
'// Declared at form level
Private m_hObject As intptr '// Holds the object for the state of the application


Dim stMsgJ1850(0 To 3) As icsSpyMessageJ1850
Dim lResult As Long

'//Fill in first header
stMsgJ1850(0).Header1 = &H1
stMsgJ1850(0).Header2 = &H2
stMsgJ1850(0).Header3 = &H0
stMsgJ1850(0).NumberBytesHeader = 3

'//Fill in data
stMsgJ1850(0).Data1 = &H4
stMsgJ1850(0).Data2 = &H5
stMsgJ1850(0).Data3 = &H6
stMsgJ1850(0).Data4 = &H7
stMsgJ1850(0).Data5 = &H8
stMsgJ1850(0).Data6 = &H9
stMsgJ1850(0).Data7 = &H10
stMsgJ1850(0).Data8 = &H11
stMsgJ1850(0).NumberBytesData = 8

'//Fill in data
stMsgJ1850(1).NumberBytesHeader = 0
stMsgJ1850(1).Data1 = &H12
stMsgJ1850(1).Data2 = &H13
stMsgJ1850(1).Data3 = &H14
stMsgJ1850(1).Data4 = &H15
stMsgJ1850(1).Data5 = &H16
stMsgJ1850(1).NumberBytesData = 5

'// Transmit the assembled message
lResult = icsneoTxMessages(m_hObject, stMsgJ1850(0), NETID_ISO, 2)

'// Test the returned result
If Not CBool(lResult) Then
    MsgBox("Problem Transmitting Message")
End If
```
