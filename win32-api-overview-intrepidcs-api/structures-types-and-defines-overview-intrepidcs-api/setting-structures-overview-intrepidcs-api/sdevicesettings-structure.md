# SDeviceSettings Structure

This structure defines a layout for setting device settings for various devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec(align(2))
{
   unsigned int uiDevice;
    union {
           SFireSettings fire;
           SFire2Settings fire2;
           SVCAN3Settings vcan3;
           SRADGalaxySettings radgalaxy;
           SRADStar2Settings radstar2;
           SVCAN4Settings vcan4;
           SVCAN412Settings vcan4_12;
           SVividCANSettings vividcan;
           SRADPlutoSettings pluto;
           SRADSuperMoonSettings supermoon;
       } Settings;
} SDeviceSettings;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SDeviceSettings
  Dim uiDevice As UInt32
  Dim Settings As HardwareSettingsToUse '//HardwareSettingsToUse with correct Struct
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct SDeviceSettings
{
public UInt32 uiDevice;
public HardwareSettingsToUse Settings;  //HardwareSettingsToUse with correct Struct
}
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| uiDevice\_en | <p>Set to indicate the type of hardware that is trying to be accessed.</p><p>DeviceFireSettingsType = 0</p><p>DeviceFireVnetSettingsType = 1</p><p>DeviceFire2SettingsType = 2</p><p>DeviceVCAN3SettingsType = 3</p><p>DeviceRADGalaxySettingsType = 4</p><p>DeviceRADStar2SettingsType = 5</p><p>DeviceVCAN4SettingsType = 6</p><p>DeviceVCAN412SettingsType = 7</p><p>DeviceVividCANSettingsType = 8</p><p>DeviceECU_AVBSettingsType = 9</p><p>DeviceRADSuperMoonSettingsType = 10</p><p>DeviceRADMoon2SettingsType = 11</p><p>DeviceRADPlutoSettingsType = 12</p><p>DeviceRADGigalogSettingsType = 13</p><p>DeviceVCANRFSettingsType = 14</p><p>DeviceEEVBSettingsType = 15</p><p>DeviceVCAN4IndSettingsType = 16</p><p>DeviceNeoECU12SettingsType = 17</p><p>DeviceFlexVnetzSettingsType = 18</p><p>DeviceCANHUBSettingsType = 19</p><p>DeviceIEVBSettingsType = 20</p><p>DeviceOBD2SimSettingsType = 21</p><p>DeviceCMProbeSettingsType = 22</p><p>DeviceOBD2ProSettingsType = 23</p><p>DeviceRedSettingsType = 24</p><p>DeviceRADPlutoSwitchSettingsType = 25</p><p>DeviceRADJupiterSettingsType = 26</p><p>DeviceFire3SettingsType = 27</p><p>DeviceRadMoonDuoSettingsType = 28</p> |
| settings     | <p>Set to the type for the hardware settings are going to be read from.</p><p>Unions can be used in C++. Other languages this needs to be set. VB Example for RAD Galaxy</p><p>&#x3C;StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure SDeviceSettings</p><p>Dim uiDevice As UInt32Dim Settings As SRADGalaxySettings</p><p>End Structure</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

****
