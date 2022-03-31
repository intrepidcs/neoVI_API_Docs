# Valid parameter names for the SetDeviceParameter and GetDeviceParameter methods

The sections below list all of the valid device parameters for each supported neoVI device.

**neoVI Fire Parameters**

The valid parameters for a neoVI Fire device are listed below. See [SFireSettingsStructure](sfiresettings-structure.md) for a listing of the valid values for each parameter.

can1 can2 can3 can4 (see [CAN Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#can-network-parameters))

swcan (see [Single Wire CAN Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#single-wire-can-network-parameters))

lsftcan (see [CAN Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#can-network-parameters))

lin1 lin2 lin3 lin4 (see [LIN Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#lin-network-parameters))

cgi\_baud

cgi\_tx\_ifs\_bit\_times

cgi\_rx\_ifs\_bit\_times

cgi\_chksum\_enable

network\_enables

network\_enabled\_on\_boot

pwm\_man\_timeout

pwr\_man\_enable

misc\_io\_initial\_ddr

misc\_io\_initial\_latch

misc\_io\_analog\_enable

misc\_io\_report\_period

misc\_io\_on\_report\_events

ain\_sample\_periodain\_threshold

iso15765\_separation\_time\_offsetiso9141\_kwp\_settings (see [ISO9141\_KWP Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#iso9141\_kwp-network-parameters))

perf\_en

iso\_parity

iso\_msg\_termination

network\_enables\_2

**valueCAN3 Parameters**

can1 can2 (see [CAN Network Parameters](valid-parameter-names-for-the-setdeviceparameter-and-getdeviceparameter-methods.md#can-network-parameters))

network\_enables

network\_enabled\_on\_boot

iso15765\_separation\_time\_offset

perf\_en

misc\_io\_initial\_ddr

misc\_io\_initial\_latch

misc\_io\_report\_period

misc\_io\_on\_report\_events

#### **CAN Network Parameters**

The valid parameters for CAN network settings on a neoVI device are listed below. Substitue the number of the CAN channel on the device for the 'x' . The current valid CAN network specifiers are can1 through can4, depending the capabilities of the device. See [CAN\_SETTINGSStructure](sub-setting-structures-overview-intrepidcs-api/can\_settings-structure.md) for a listing of valid values for each parameter.

canx/Mode

canx/SetBaudrate

canx/Baudrate

canx/NetworkType

canx/TqSeg1

canx/TqSeg2

canx/TqProp

canx/TqSync

canx/BRP

canx/auto\_baud

#### **Single Wire CAN Network Parameters**

The valid parameters for single wire CAN network settings on a neoVI device are listed below. See [SWCAN\_SETTINGSStructure](sub-setting-structures-overview-intrepidcs-api/swcan\_settings-structure.md) for a listing of valid values for each parameter.

swcan/Mode

swcan/SetBaudrate

swcan/Baudrate

swcan/NetworkType

swcan/TqSeg1

swcan/TqSeg2

swcan/TqProp

swcan/TqSync

swcan/BRP

swcan/high\_speed\_auto\_switch

swcan/auto\_baud

#### **LIN Network Parameters**

The valid parameters for a LIN network on a neoVI device are listed below. Substitute the number of the LIN channel on the device for the ‘x’. The current valid LIN network specifiers are lin1 through lin4. See [LIN\_SETTINGSStructure](sub-setting-structures-overview-intrepidcs-api/lin\_settings-structure.md) for a listing of valid values for each parameter.

linx/Baudratelinx/spbrg

linx/brgh

linx/MasterResistor

linx/Mode

#### **ISO9141\_KWP Network Parameters**

The valid parameters for the ISO9141\_KWP Network are listed below. For the iso9141\_kwp\_settings/init\_steps/x/ parameters, substitute the number of the desired step for the ‘x’. The current valid init\_steps range is 0 through 15, for a total of 16 steps.

iso9141\_kwp\_settings/Baudrate

iso9141\_kwp\_settings/spbrg

iso9141\_kwp\_settings/brgh

iso9141\_kwp\_settings/init\_steps/x/time\_500us

iso9141\_kwp\_settings/init\_steps/x/k

iso9141\_kwp\_settings/init\_steps/x/l

iso9141\_kwp\_settings/init\_step\_count

iso9141\_kwp\_settings/p2\_500us

iso9141\_kwp\_settings/p3\_500us

iso9141\_kwp\_settings/p4\_500us

iso9141\_kwp\_settings/chksum\_enabled
