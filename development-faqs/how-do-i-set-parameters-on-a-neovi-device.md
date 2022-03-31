# How do I set parameters on a neoVI device?

The API offers a few different ways to alter the settings in the hardware. Each has their own advantages.

*   Device specific Get and Set Settings functions:

    Each hardware device has a specific function for getting and setting settings with a unique structure breaking out all the settings for that device. The [Device Settings Function](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/) page has detailed information on the functions and structures. The advantage of this method is access to all the settings of the hardware.
*   [SetBitRate](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/setbitrate-method-intrepidcs-api.md) function:

    This function gives the ability to set baud rates for any device. This command is not device specific. The same command will work on a ValueCAN 3, Plasma, RAD Galaxy, so on, and so on. The disadvantage is a limitation on the settings that can be configured. This is good for simple baud rate changes for setups that are device independent.
*   Get and Set Device Parameter:

    To set individual parameters the [GetDeviceParameters](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/getdeviceparameters-method-intrepidcs-api.md) and [SetDeviceParameters](../win32-api-overview-intrepidcs-api/device-settings-functions-overview-intrepidcs-api/general-device-settings-intrepidcs-api/setdeviceparameters-method-intrepidcs-api.md) functions can be used. This function set uses a string of specific parameters to get or set without using a device specific structure. The same parameter strings without regard to the type of device you are connected to. For instance, the string for setting the baud rate on the first CAN channel on a ValueCAN3 and a neoVI Fire are the same.
