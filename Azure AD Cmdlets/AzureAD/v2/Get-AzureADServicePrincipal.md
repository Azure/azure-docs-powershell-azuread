---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 8EAAE8EA-44D5-4B28-A940-28085547083A
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipal

## SYNOPSIS
Gets a service principal.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADServicePrincipal [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADServicePrincipal [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADServicePrincipal -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADServicePrincipal** cmdlet gets a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve all service principal from the directory
```
PS C:\> Get-AzureADServicePrincipal

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
00221b6f-4387-4f3f-aa85-34316ad7f956 e5e29b8a-85d9-41ea-b8d1-2162bd004528 Tenant Schema Extension App
012f6450-15be-4e45-b8b4-e630f0fb70fe 00000005-0000-0ff1-ce00-000000000000 Microsoft.YammerEnterprise
06ab01eb-3e77-4d14-ae31-322c7730a65b 09abbdfd-ed23-44ee-a2d9-a627aa1c90f3 ProjectWorkManagement
092aaf41-23e8-46eb-8c3d-fc0ee91cc62f 507bc9da-c4e2-40cb-96a7-ac90df92685c Office365Reports
0ac66e69-5502-4406-a294-6dedeadc8cab 2cf9eb86-36b5-49dc-86ae-9a63135dfa8c AzureTrafficManagerandDNS
0c0a6d9d-48c0-4aa7-b484-4e46f77d8ed9 0f698dd4-f011-4d23-a33e-b36416dcb1e6 Microsoft.OfficeClientService
0cbef08e-a4b5-4dd9-865e-8f521c1c5fb4 0469d4cd-df37-4d93-8a61-f8c75b809164 Microsoft Policy Administration Service
0ea80ff0-a9ea-43b6-b876-d5989efd8228 00000009-0000-0000-c000-000000000000 Microsoft Power BI Reporting and Analytics</dev:code>
```

This command retrieves all service principal from the directory. 

### Example 2: Retrieve a service principal by ID
```
PS C:\> $ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> Get-AzureADServicePrincipal $ServicePrincipalId

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
00221b6f-4387-4f3f-aa85-34316ad7f956 e5e29b8a-85d9-41ea-b8d1-2162bd004528 Tenant Schema Extension App
```

The first command gets the ID of a service principal by using the [Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md) cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets the service principal identified by $ServicePrincipalId. 

## PARAMETERS

### -All
If true, return all serviceprincipal objects. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a service principal in Azure AD.

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

[Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)

[Remove-AzureADServicePrincipal](./Remove-AzureADServicePrincipal.md)

[Set-AzureADServicePrincipal](./Set-AzureADServicePrincipal.md)
