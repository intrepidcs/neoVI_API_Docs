# GetErrorInfo Method - intrepidcs API

This method returns a text description of an intrepidcs API error number.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoGetErrorInfo(int lErrorNumber, 
            TCHAR *szErrorDescriptionShort,  
            TCHAR  *szErrorDescriptionLong,
            int *lMaxLengthShort,
            int *lMaxLengthLong,
            int *lErrorSeverity,
            int *lRestartNeeded);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoGetErrorInfo Lib "icsneo40.dll" _
            (ByVal lErrorNumber As Int32, _
            ByVal sErrorDescriptionShort As String, _
            ByVal sErrorDescriptionLong As String, _
            ByRef lMaxLengthShort As Int32, _
            ByRef lMaxLengthLong As Int32, _
            ByRef lErrorSeverity As Int32, _
            ByRef lRestartNeeded As Int32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport("icsneo40.dll")]
public static extern int icsneoGetErrorInfo(int iErrorNumber,
            StringBuilder sErrorDescriptionShort, 
            StringBuilder sErrorDescriptionLong, 
            ref int iMaxLengthShort, 
            ref int iMaxLengthLong, 
            ref int lErrorSeverity , 
            ref int lRestartNeeded);
```
{% endtab %}
{% endtabs %}

**Parameters**

_lErrorNumber_\
\[in] This is the number of the error message returned from [GetErrorMessages](geterrormessages-method-intrepidcs-api.md). A separate topic describes the possible values for [error messages](error-messages-intrepidcs-api.md).

_sErrorDescriptionShort_\
\[out] This is short description of the error. This parameter should be sized to include up to 255 characters including the NULL terminator.

_sErrorDescriptionLong_\
\[out] This is longer more detailed description of the error. This parameter should be sized to include up to 255 characters including the NULL terminator.\
\
_lMaxLengthShort_\
\[in] This is the size in characters of the _<mark style="color:orange;">sErrorDescriptionShort</mark>_ array that is being passed in. This value must be 255 or less.\
\
_lMaxLengthLong_\
\[in] This is the size in characters of the _<mark style="color:orange;">sErrorDescriptionLong</mark>_ array that is being passed in. This value must be 255 or less.

_lErrorSeverity_\
\[out] This indicates the error severity. This is estimated severity for the application and doesn't have significant meaning. See Table 1 below for more information.

_lRestartNeeded_\
\[out] If 1 it is recommend that the application close communications with the DLL and reopen it.

**Return Values**

If the error number was found successfully the return value will be non-zero.

**Remarks**

None.

**Table 1 - Descriptions of Error Severity**

| Error Severity                                                                  | Description                                                            |
| ------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| <mark style="color:blue;">const unsigned long</mark> icsspyErrCritical=0x10;    | A critical error which affects operation or accuracy                   |
| <mark style="color:blue;">const unsigned long</mark> icsspyErrExclamation=0x30; | An important error which may be critical depending on the application. |
| <mark style="color:blue;">const unsigned long</mark> icsspyErrInformation=0x40; | An error which probably does not need attention.                       |
| <mark style="color:blue;">const unsigned long</mark> icsspyErrQuestion=0x20;    | An error which is not understood.                                      |

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
// Read the errors from the DLL
lResult = icsneoGetErrorMessages(hObject,iErrors,&lNumberOfErrors);

if (lResult == 0)
    MessageBox(hWnd,TEXT("Problem Reading errors"),TEXT("neoVI Example"),0);

// dump the neoVI errors
if (lNumberOfErrors > 0)
{
    for (lCount=0;lCount <lNumberOfErrors;lCount++)
    {

        wsprintf(szOut,TEXT("Error %d - "),iErrors[lCount]);
            OutputDebugString(szOut);
            icsneoGetErrorInfo(iErrors[lCount],szDescriptionShort,szDescriptionLong,
                        &lMaxLengthShort,&lMaxLengthLong,&lErrorSeverity,&lRestartNeeded);

        OutputDebugString(szDescriptionShort);
        OutputDebugString(TEXT("\n"));
    }
}
else
    OutputDebugString(TEXT("No Errors to report\n"));
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Public Function icsneoGetDLLErrorInfo(ByVal lErrorNum As Int32, ByRef sErrorShort As String, ByRef sErrorLong As String, ByRef lSeverity As Int32, ByRef bRestart As Int32) As Boolean

Dim lErrorLongLength As Int32
Dim lErrorShortLength As Int32
Dim lRestart As Int32
Dim lResult As Int32

    sErrorLong = New String(Chr(0), 255)
    sErrorShort = New String(Chr(0), 255)
    lErrorLongLength = 255
    lErrorShortLength = 255
    lResult = icsneoGetErrorInfo(lErrorNum, sErrorShort, sErrorLong, lErrorShortLength, lErrorLongLength, lSeverity, lRestart)

    sErrorShort = Left(sErrorShort, lErrorShortLength)
    sErrorLong = Left(sErrorLong, lErrorLongLength)
    bRestart = CBool(lRestart)
    icsneoGetDLLErrorInfo = CBool(lResult)
End Function

**This function reads errors and loads them into a list box**

Private Sub cmdGetErrors_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles cmdGetErrors.Click

Dim lResult As Integer '//Storage for result of Function Call
Dim lErrors(600) As Int32 '//Array for Error information
Dim lNumberOfErrors As Integer '//Storage for Number of Errors
Dim lCount As Integer '//Counter
Dim sErrorShort As String '//String Holding Short Error Name
Dim sErrorLong As String '//String Holding Long Error Name
Dim iSeverity As Int32 '//Storage for Level of error
Dim bRestart As Int32 '//flag for if Restart is required

    '// Read Out the errors
    lResult = icsneoGetErrorMessages(m_hObject, lErrors(0), lNumberOfErrors)
    '// Test the returned result
    If Not CBool(lResult) Then
        MsgBox("Problem Reading Errors")
    Else
        '//List Error information
        lstErrorHolder.Items.Clear()
        For lCount = 1 To lNumberOfErrors
            Call icsneoGetDLLErrorInfo(lErrors(lCount - 1), sErrorShort, sErrorLong, iSeverity, bRestart)
            lstErrorHolder.Items.Add(sErrorShort + " - Description" + _
                    sErrorLong + " - Errornum: " + Convert.ToString(lErrors(lCount - 1)))
        Next lCount
    End If
End Sub
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
private void cmdGetErrors_Click(object sender, System.EventArgs e)
{
    int iResult = 0; //Storage for Result of Call
    int[] iErrors = new int[600]; //Array for Error Numbers
    int iNumberOfErrors = 0; // Storage for number of errors
    int iCount= 0; //Counter
    int iSeverity =0; //tells the Severity of Error
    int iMaxLengthShort = 0; //Tells Max length of Error String
    int iMaxLengthLong = 0; //Tells Max Length of Error String
    int lRestart = 0; //tells if a restart is needed
    StringBuilder sErrorShort = new StringBuilder(256); //String for Error
    StringBuilder sErrorLong = new StringBuilder(256); //String for Error
    iMaxLengthShort = 1; //Set initial conditions
    iMaxLengthLong = 1; //Set initial conditions
    // Read Out the errors
    iResult = icsNeoDll.icsneoGetErrorMessages(m_hObject,ref iErrors[0],ref iNumberOfErrors);
    // Test the returned result
    if(iResult == 0)
    {
        MessageBox.Show ("Problem Reading Errors");
    }
    else
    {
        if(iNumberOfErrors != 0)
        {
            for(iCount=0;iCount< iNumberOfErrors;iCount++)
            {
                //Get Text Description of the Error
                iResult = icsNeoDll.icsneoGetErrorInfo(iErrors[iCount],
                    sErrorShort, sErrorLong ,ref iMaxLengthShort , ref iMaxLengthLong, ref iSeverity,ref lRestart);
                lstErrorHolder.Items.Add (sErrorShort + " - Description " + sErrorLong + " - Errornum: " + iErrors[iCount]);
            }
        }
    }
}
```
{% endtab %}
{% endtabs %}
