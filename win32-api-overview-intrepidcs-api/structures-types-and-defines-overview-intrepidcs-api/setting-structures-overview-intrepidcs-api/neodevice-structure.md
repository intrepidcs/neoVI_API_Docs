# NeoDevice Structure

A structure used by [FindNeoDevices](../../deprecated-functions-overview-intrepidcs-api/findneodevices-method-intrepidcs-api.md) and [OpenNeoDevice](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) to locate and open neoVI devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct
{
    unsigned long DeviceType;
    int Handle;
    int NumberOfClients;
    int SerialNumber;
    int MaxAllowedClients;
}NeoDevice;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
'//Structure for neoVI device types
Public Structure NeoDevice
    Dim DeviceType As Int32
    Dim Handle As Int32
    Dim NumberOfClients As Int32
    Dim SerialNumber As Int32
    Dim MaxAllowedClients As Int32
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct NeoDevice
{
    public Int32 DeviceType;
    public Int32 Handle;
    public Int32 NumberOfClients;
    public Int32 SerialNumber;
    public Int32 MaxAllowedClients;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

Instances of this structure are initialized and set by calling [FindNeoDevices](../../deprecated-functions-overview-intrepidcs-api/findneodevices-method-intrepidcs-api.md). Then the structure is used by [OpenNeoDevice](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) to make a physical connection to a neoVI device.

| Item            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DeviceType      | <p>A bit-wise field that indicates the type of neoVI device that the structure represents. The currently supported types are :</p><p>NEODEVICE_BLUE = 1</p><p>NEODEVICE_DW_VCAN = 4</p><p>NEODEVICE_VCAN41 = 7</p><p>NEODEVICE_FIRE = 8</p><p>NEODEVICE_VCAN3 = 16</p><p>NEODEVICE_RED = 64</p><p>NEODEVICE_ECU = 128</p><p>NEODEVICE_IEVB = 256</p><p>NEODEVICE_PENDANT = 512</p><p>NEODEVICE_PLASMA = &#x26;H31000</p><p>NEODEVICE_FIRE_VNET = &#x26;H2000</p><p>NEODEVICE_NEOANALOG = &#x26;H4000</p><p>NEODEVICE_ION = &#x26;H140000</p><p>NEODEVICE_VCANFD = &#x26;H200000</p><p>NEODEVICE_VCAN42 = &#x26;H400000</p><p>NEODEVICE_EEVB = &#x26;H1000000</p><p>NEODEVICE_VCANRF = &#x26;H2000000</p><p>NEODEVICE_FIRE2 = &#x26;H4000000</p><p>NEODEVICE_FLEX = &#x26;H8000000</p><p>NEODEVICE_RADGALAXY = &#x26;H10000000</p><p>NEODEVICE_RADSTAR2 = &#x26;H20000000</p><p>NEODEVICE_OBD2_SIM = &#x26;H80000000</p><p>NEODEVICE_ALL = &#x26;HFFFFBFFF</p> |
| Handle          | The device handle used by the API for opening a neoVI device                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NumberOfClients | Reserved for future use                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SerialNumber    | Serial number of the neoVI device                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| MaxAllowClients | Reserved for future use                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
