# How do I detect and handle disconnects?

If the neoVI is removed from the computer or stops responding, most API calls will generate a disconnect error. If you receive a return value from an API call that indicates an error occurred, you must call the GetLastAPIError method. If the error is `NEOVI_ERROR_DLL_NEOVI_NO_RESPONSE` then the neoVI has either been unplugged or is not responding.

To recover from this condition follow these steps:

* Plug the neoVI back in, or in the case of the neoVI not responding, remove and then plug back in.
* Call the [ClosePort](../win32-api-overview-intrepidcs-api/basic-functions-overview-intrepidcs-api/closeport-method-intrepidcs-api.md) method.
* Call the [OpenNeoDevice](../win32-api-overview-intrepidcs-api/basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) method using the same parameters are before.

The following API functions will generate the NEOVI\_ERROR\_DLL\_NEOVI\_NO\_RESPONSE error:

| Function                                                                                                                                                                                                    |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [GetMessages](../win32-api-overview-intrepidcs-api/message-functions-overview-intrepidcs-api/getmessages-method-intrepidcs-api.md)                                                                          |
| [TxMessages](../win32-api-overview-intrepidcs-api/message-functions-overview-intrepidcs-api/txmessages-method-intrepidcs-api.md)                                                                            |
| [WaitForRxMessagesWithTimeOut](../win32-api-overview-intrepidcs-api/message-functions-overview-intrepidcs-api/waitforrxmessageswithtimeout-method-intrepidcs-api.md)                                        |
| [GetTimeStampForMsg](../win32-api-overview-intrepidcs-api/message-functions-overview-intrepidcs-api/gettimestampformsg-method-intrepidcs-api.md)                                                            |
| [EnableNetworkCom](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/enablenetworkcom-method-intrepidcs-api.md)                                                             |
| [GetConfiguration](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/getconfiguration-method-intrepidcs-api.md)                                                        |
| [SendConfiguration](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/sendconfiguration-method-intrepidcs-api.md)                                                      |
| [GetFireSettings](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/neovi-fire-intrepidcs-api/getfiresettings-method-intrepidcs-api.md)                                |
| [SetFireSettings](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/neovi-fire-intrepidcs-api/setfiresettings-method-intrepidcs-api.md)                                |
| [GetVCAN3Settings](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/valuecan3-intrepidcs-api/getvcan3settings-method-intrepidcs-api.md)                               |
| [SetVCAN3Settings](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/valuecan3-intrepidcs-api/setvcan3settings-method-intrepidcs-api.md)                               |
| [SetBitRate](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/setbitrate-method-intrepidcs-api.md)                             |
| [GetDeviceParameters](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/getdeviceparameters-method-intrepidcs-api.md)           |
| [SetDeviceParameters](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/setdeviceparameters-method-intrepidcs-api.md)           |
| [ScriptLoad](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptload-method-intrepidcs-api.md)                       |
| [ScriptStart](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptstart-method-intrepidcs-api.md)                     |
| [ScriptStop](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptstop-method-intrepidcs-api.md)                       |
| [ScriptClear](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptclear-method-intrepidcs-api.md)                     |
| [ScriptStartFBlock](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptstartfblock-method-intrepidcs-api.md)         |
| [ScriptStopFBlock](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptstopfblock-method-intrepidcs-api.md)           |
| [ScriptGetFBlockStatus](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptgetfblockstatus-method-intrepidcs-api.md) |
| [ScriptGetScriptStatus](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptgetscriptstatus-method-intrepidcs-api.md) |
| [ScriptReadAppSignal](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptreadappsignal-method-intrepidcs-api.md)     |
| [ScriptWriteAppSignal](../win32-api-overview-intrepidcs-api/deprecated-functions-overview-intrepidcs-api/coremini-script-interface-overview-intrepidcs-api/scriptwriteappsignal-method-intrepidcs-api.md)   |
| ScriptReadRxMessage                                                                                                                                                                                         |
| ScriptReadTxMessage                                                                                                                                                                                         |
| ScriptWriteRxMessage                                                                                                                                                                                        |
| ScriptWriteTxMessage                                                                                                                                                                                        |
| ScriptReadISO15765\_2\_TxMessage                                                                                                                                                                            |
| ScriptWriteISO15765\_2\_TxMessage                                                                                                                                                                           |
