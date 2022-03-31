# ISO15765\_ReceiveMessage Method - intrepidcs API

**This method configures a receive message using ISO15765-2 on a CAN network. icsneoISO15765\_EnableNetwroks must be called before using icsneoISO15765\_ReceiveMessage. PCI bytes and Flow control decoding is taken care of by the dll for the transaction.**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
void _stdcall icsneoISO15765_ReceiveMessage(void * hObject, unsigned long ulNetworkID,stCM_ISO157652_RxMessage *pMsg);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoISO15765_ReceiveMessage Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByVal ulNetworkID As Integer, ByRef pMsg As stCM_ISO157652_RxMessage) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoISO15765_ReceiveMessage(IntPtr hObject,Int32 ulNetworkID,ref stCM_ISO157652_RxMessage pMsg);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle which specifies the driver object created with the OpenPort method.

_ulIndex_\
&#x20;   \[in] Specifies the Index to configure, 10 elements 0-9.

stCM\_ISO157652\_RxMessage

\[in] This is the address of the [stCM\_ISO15765\_RxMessage](../../structures-types-and-defines-overview-intrepidcs-api/setting-structures-overview-intrepidcs-api/stcm\_iso157652\_rxmessage-structure.md) structure. The structure contains the properties for the multi frame message transaction.

**Return Values**

None.

**Remarks**

None.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
int lResult;
stCM_ISO157652_RxMessage flow_cntrl_msg;

memset(&flow_cntrl_msg,0,sizeof(flow_cntrl_msg));
lResult = icsneoISO15765_EnableNetworks(m_hObject, NETID_HSCAN);

//Build structure for message
flow_cntrl_msg.vs_netid = NETID_HSCAN;
flow_cntrl_msg.padding = 0xAA; //Set Padding Byte
flow_cntrl_msg.id = 0x7E0; //ArbID of the message
flow_cntrl_msg.id_mask = 0xFFF; //The flow control arb filter mask (response id from receiver)
flow_cntrl_msg.fc_id = 0x7E8; //ArbID for the flow control Frame
flow_cntrl_msg.blockSize = 100;
flow_cntrl_msg.stMin = 100;
flow_cntrl_msg.cf_timeout = 1000;

//Set flags for Padding and ID information.
flow_cntrl_msg.paddingEnable = true;
flow_cntrl_msg.id_29_bit_enable = false;
flow_cntrl_msg.fc_id_29_bit_enable = false;
flow_cntrl_msg.ext_address_enable = false;
flow_cntrl_msg.fc_ext_address_enable = false;
flow_cntrl_msg.overrideSTmin = false;
flow_cntrl_msg.overrideBlockSize = false;

lResult = icsneoISO15765_ReceiveMessage(m_hObject, 0, &flow_cntrl_msg);
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
int lResult;
String sTempNetwork;
stCM_ISO157652_RxMessage flow_cntrl_msg = new stCM_ISO157652_RxMessage();

lResult = icsNeoDll.icsneoISO15765_EnableNetworks(m_hObject, Convert.ToInt32(eNETWORK_ID.NETID_HSCAN));

//Build structure for message
flow_cntrl_msg.vs_netid = Convert.ToInt16(eNETWORK_ID.NETID_HSCAN);
flow_cntrl_msg.padding = 0xAA; //Set Padding Byte
flow_cntrl_msg.id = 0x7E0 //ArbID of the message
flow_cntrl_msg.id_mask = 0xFFF; //The flow control arb filter mask (response id from receiver)
flow_cntrl_msg.fc_id = 0x7E8; //ArbID for the flow control Frame
flow_cntrl_msg.blockSize = 100;
flow_cntrl_msg.stMin = 100;
flow_cntrl_msg.cf_timeout = 1000;

//Set flags for Padding and ID information.
flow_cntrl_msg.flags = 0;
int iFlags = Convert.ToInt32(stCM_ISO157652_RxMessage_Flags.enableFlowControlTransmission);
iFlags = (iFlags | Convert.ToInt32(CSnet.stCM_ISO157652_TxMessage_Flags.paddingEnable));
flow_cntrl_msg.flags = Convert.ToUInt16(iFlags);

lResult = icsNeoDll.icsneoISO15765_ReceiveMessage(m_hObject, 0, ref flow_cntrl_msg);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim lResult As Integer
Dim flow_cntrl_msg As stCM_ISO157652_RxMessage

lResult = icsneoISO15765_EnableNetworks(m_hObject, NETID_HSCAN)

'//Build structure for message
flow_cntrl_msg.vs_netid = NETID_HSCAN
flow_cntrl_msg.padding = &HAA '//Set Padding Byte
flow_cntrl_msg.id = &H7E0 '//ArbID of the message
flow_cntrl_msg.id_mask = &HFFF '//The flow control arb filter mask (response id from receiver)
flow_cntrl_msg.fc_id = &H7E8 '//ArbID for the flow control Frame
flow_cntrl_msg.blockSize = 100
flow_cntrl_msg.stMin = 100
flow_cntrl_msg.cf_timeout = 1000

'//Set flags for Padding and ID information.
flow_cntrl_msg.flags = Convert.ToUInt32(stCM_ISO157652_RxMessage_Flags.enableFlowControlTransmission)
flow_cntrl_msg.flags = CUShort(flow_cntrl_msg.flags Or stCM_ISO157652_TxMessage_Flags.paddingEnable)

lResult = icsneoISO15765_ReceiveMessage(m_hObject, 0, flow_cntrl_msg)
```
{% endtab %}
{% endtabs %}
