# RAD\_GPTP\_SETTINGS Structure

**This structure defines various settings for the gPTP**

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec (align(2))
{
   uint32_t neighborPropDelayThresh;
   uint32_t sys_phc_sync_interval;
   int8_t logPDelayReqInterval;
   int8_t logSyncInterval;
   int8_t logAnnounceInterval;
   uint8_t profile;
   uint8_t priority1;
   uint8_t clockclass;
   uint8_t clockaccuracy;
   uint8_t priority2;
   uint16_t offset_scaled_log_variance;
   uint8_t gPTPportRole;
   uint8_t gptpEnabledPort;
   uint32_t rsvd0;
   uint32_t rsvd1;
   uint32_t rsvd2;
   uint32_t rsvd3;
}RAD_GPTP_SETTINGS;
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure RAD_GPTP_SETTINGS
   Dim neighborPropDelayThresh As UInt32
   Dim sys_phc_sync_interval As UInt32
   Dim logPDelayReqInterval As Byte
   Dim logSyncInterval As Byte
   Dim logAnnounceInterval As Byte
   Dim profile As Byte
   Dim priority1 As Byte
   Dim clockclass As Byte
   Dim clockaccuracy As Byte
   Dim priority2 As Byte
   Dim offset_scaled_log_variance As UInt16
   Dim gPTPportRole As Byte
   Dim gptpEnabledPort As Byte
   Dim rsvd0 As UInt32
   Dim rsvd1 As UInt32
   Dim rsvd2 As UInt32
   Dim rsvd3 As UInt32
End Structure
```
{% endtab %}

{% tab title="C# .NET Declare" %}
```csharp
[StructLayout(LayoutKind.Sequential,Pack=2)]
public struct RAD_GPTP_SETTINGS
{
   public UInt32 neighborPropDelayThresh;
   public UInt32 sys_phc_sync_interval;
   public byte logPDelayReqInterval;
   public byte logSyncInterval;
   public byte logAnnounceInterval;
   public byte profile;
   public byte priority1;
   public byte clockclass;
   public byte clockaccuracy;
   public byte priority2;
   public UInt16 offset_scaled_log_variance;
   public byte gPTPportRole;
   public byte gptpEnabledPort;
   public UInt32 rsvd0;
   public UInt32 rsvd1;
   public UInt32 rsvd2;
   public UInt32 rsvd3;
   }
```
{% endtab %}
{% endtabs %}

**Remarks**

| Item                          | Description                                                                                                                                                                                                                                     |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| neighborPropDelayThresh       | Threshold value for neighbor propagation delay. A Device will be identified as non-AS Capable if pDelay exceeds this value                                                                                                                      |
| sys\_phc\_sync\_interval      | Not Defined                                                                                                                                                                                                                                     |
| logPDelayReqInterval          | <p>Delay Request Interval<br>Value = log2(Interval in Seconds)</p>                                                                                                                                                                              |
| logSyncInterval               | <p>Sync Interval<br>Value = log2(Interval in Seconds)</p>                                                                                                                                                                                       |
| logAnnounceInterval           | <p>Announce Interval<br>Value = log2(Interval in Seconds)</p>                                                                                                                                                                                   |
| profile                       | <p>Set the gPTP Profile<br>0 = Standard, 1=Automotive</p>                                                                                                                                                                                       |
| priority1                     | Priority1 sets the ordering priority. Lower values set a better ClockMaster. See gPTP spec, 8021AS for more details and restrictions.                                                                                                           |
| clockclass                    | clockClass gives the traceability of the synchronized time sent by the Master in Grandmaster mode. See gPTP spec, 8021AS for more details.                                                                                                      |
| clockaccuracy                 | clockAccuracy sets the time Accuracy of the ClockMaster. Lower values indicate better clocks. See gPTP spec, 8021AS for more details.                                                                                                           |
| priority2                     | priority2 uses a similar scheme as priority1. See gPTP spec, 8021AS for more details.                                                                                                                                                           |
| offset\_scaled\_log\_variance | This parameter is an estimate of the Variance in PTP. See gPTP spec, 8021AS for more details.                                                                                                                                                   |
| gPTPportRole                  | <p>Sets the gPTP port Role.<br>0 = Master, 1=Slave</p>                                                                                                                                                                                          |
| gptpEnabledPort               | <p>Sets the Channel to use for gPTP<br>0 = Disabled, 1 = OpEth1, 2 = OpEth2, 3 = OpEth3<br>4 = OpEth4, 5 = OpEth5, 6 = OpEth6, 7 = OpEth7<br>8 = OpEth8, 9 = OpEth9, 10 = OpEth10, 11 = OpEth11<br>12 = OpEth12, 13 = StdEth1, 14 = StdEth2</p> |
| rsvd0                         | Reserved                                                                                                                                                                                                                                        |
| rsvd1                         | Reserved                                                                                                                                                                                                                                        |
| rsvd2                         | Reserved                                                                                                                                                                                                                                        |
| rsvd3                         | Reserved                                                                                                                                                                                                                                        |
