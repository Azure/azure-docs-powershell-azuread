---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnectorGroupMembers

## SYNOPSIS
The Get-AzureADApplicationProxyConnectorGroupMembers gets all the Application Proxy connectors associated with the given connector group. 

## SYNTAX

## DESCRIPTION
The Get-AzureADApplicationProxyConnectorGroupMembers gets all the Application Proxy connectors associated with the given connector group. 

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyConnectorGroupMembers -Id ba07e273-6b9e-4567-afe4-efddac32509d

Id                                   MachineName     ExternalIp   Status
--                                   -----------     ----------   ------
969eddd2-ad11-47ca-92ba-4442b9901edf vm-test-010 13.93.84.164 active
ea4a4b91-aace-4e8b-b81a-b2f6429a477e test-vm-conn1 52.18.9.115 active
```

The output of this command, showing all the connectors in the group.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
