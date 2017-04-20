# Where can I find the PowerShell log file?

Azure AD PowerShell maintains a log file for diagnostic purposes. You can find this file here:

```powershell
C:\Users\<alias>\AppData\Local\Microsoft\AzureAD\Powershell\AzureADPowershell_<sessionStartTimeStamp>.log
```

The log file contains a time stamped record of all actions a cmdlet has executed. You can use this to analyze errors or just follow the execution path of a cmdlet or script.
