---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: E008C14D-91DE-4CD4-BB76-6D037BB747DB
online version: 
schema: 2.0.0
---

# Get-AzureADGroup

## SYNOPSIS
Gets a group.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADGroup [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADGroup [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADGroup -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADGroup** cmdlet gets a group in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get all groups
```
PS C:\>Get-AzureADGroup


ObjectId                             DisplayName                          Description
--------                             -----------                          -----------
00628948-b509-4362-aa73-380c4dbd2a44 ADSyncBrowse
02d91535-6c02-42bc-8ede-c57189320cc0 NewGroup2
093fc0e2-1d6e-4a1b-9bf8-effa0196f1f7 All Users
0dc8d2b2-d907-42e8-8558-0add236a8408 ADSyncOperators
0e6cf869-82ca-4647-b330-420b9a6f8ef7 Temporary users team (Dynamic group)
10d81ac5-1993-434b-b74c-1dcc4fd534ea HappyThanksgiving
1e94a453-2727-47f6-b59e-d86df3494312 European teams
23af9bad-83c5-4f03-a4e4-363bd892fc56 South-West Sales team
269f90d5-93dc-4c0a-8f22-bf23da4e0c3a All FTE employees
2b559810-b5de-41a8-913f-c45a55adfc25 Exchange Trusted Subsystem           This group contains Exchange servers that run Exchange cmdlets on behalf of users via the management service.
Its members ...
31f1ff6c-d48c-4f8a-b2e1-abca7fd399df Intune Administrators                Intune Device Administrators
364e009b-fbe4-4aef-b230-2e9e8f2fe636 ADSyncPasswordSet
3d3f7196-3ec8-4076-a232-1ca30b655d1a WinRMRemoteWMIUsers__                Members of this group can access WMI resources over management protocols (such as WS-Management via the Windows Remote Man...
3df5d8b7-8af4-4536-90d6-cde4c878e252 ADSyncOperators
4370f0a6-78e9-44cb-b722-29cb5307fdba Exchange Servers                     This group contains all the Exchange servers. This group shouldn't be deleted.
47a1bff5-f449-4bfc-8772-b1515c57fec5 ExchangeLegacyInterop                This group is for interoperability with Exchange 2003 servers within the same forest.
This group should not be deleted.
```

### Example 2: Get groups that contain a search string
```
PS C:\>Get-AzureADGroup -SearchString "All"

ObjectId                             DisplayName                                 Description
--------                             -----------                                 -----------
093fc0e2-1d6e-4a1b-9bf8-effa0196f1f7 All Users
```

This command gets the groups that include the text All in their display names.

## PARAMETERS

### -All
If true, return all groups. If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
Specifies an oData v3.0 filter statement. This parameter controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
The unique identifier of a group in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.
```yaml
Type: String
Parameter Sets: GetVague
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADGroup](./New-AzureADGroup.md)
[Remove-AzureADGroup](./Remove-AzureADGroup.md)
[Set-AzureADGroup](./Set-AzureADGroup.md)


