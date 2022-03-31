# NeoDeviceEx Structure

A structure used by [FindNeoDevicesEx](../../deprecated-functions-overview-intrepidcs-api/findneodevices-method-intrepidcs-api.md) and [OpenNeoDeviceEx](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) to locate and open neoVI devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct NeoDeviceEx
{
NeoDevice neoDevice;
unsigned long FirmwareMajor;
unsigned long FirmwareMinor;
unsigned long Status; // 1=CM Running 2=Bootloader
unsigned long Reserved[16];  // may be expanded in future revisions
}NeoDeviceEx;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
'//Structure for neoVI device types
Public Structure NeoDeviceEx
    Dim neoDevice As NeoDevice
    Dim FirmwareMajor As UInt32
    Dim FirmwareMinor As UInt32
    Dim Status As UInt32 '// 1=CM Running 2=Bootloader
    Dim Reserved00 As UInt32
    Dim Reserved01 As UInt32
    Dim Reserved02 As UInt32
    Dim Reserved03 As UInt32
    Dim Reserved04 As UInt32
    Dim Reserved05 As UInt32
    Dim Reserved06 As UInt32
    Dim Reserved07 As UInt32
    Dim Reserved08 As UInt32
    Dim Reserved09 As UInt32
    Dim Reserved10 As UInt32
    Dim Reserved11 As UInt32
    Dim Reserved12 As UInt32
    Dim Reserved13 As UInt32
    Dim Reserved14 As UInt32
    Dim Reserved15 As UInt32
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
//Structure for neoVI device types
[StructLayout(LayoutKind.Sequential)]
public struct NeoDeviceEx
{
    public NeoDevice neoDevice;
    public UInt32 FirmwareMajor;
    public UInt32 FirmwareMinor;
    public UInt32 Status; // 1=CM Running 2=Bootloader
    public UInt32 Reserved00;
    public UInt32 Reserved01;
    public UInt32 Reserved02;
    public UInt32 Reserved03;
    public UInt32 Reserved04;
    public UInt32 Reserved05;
    public UInt32 Reserved06;
    public UInt32 Reserved07;
    public UInt32 Reserved08;
    public UInt32 Reserved09;
    public UInt32 Reserved10;
    public UInt32 Reserved11;
    public UInt32 Reserved12;
    public UInt32 Reserved13;
    public UInt32 Reserved14;
    public UInt32 Reserved15;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

FindNeoDevicesEx. Then the structure is used by [OpenNeoDeviceEx](../../basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) to make a physical connection to a neoVI (ECU) device.

| Item                                          | Description                                                                                     |
| --------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| neoDevice [NeoDevice](neodevice-structure.md) | Structure that containing device information like Serial number, device type, and Device Handel |
| unsigned long FirmwareMajor                   | Returns the Major firmware version of the device                                                |
| unsigned long FirmwareMinor                   | Returns the Minor firmware version of the device                                                |
| unsigned long Status                          | <p>Tells the status of the device.</p><p>CoreMini Running = 1; Bootloader = 2;</p>              |
| unsigned long Reserved                        | Reserved for future use                                                                         |
