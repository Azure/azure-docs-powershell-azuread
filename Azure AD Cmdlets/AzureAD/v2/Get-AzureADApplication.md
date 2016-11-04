---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: FC0F8815-DEEC-4672-81A1-68A1095E5543
---

# Get-AzureADApplication

## SYNOPSIS
Gets an application.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADApplication [-Top <Int32>] [-Filter <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADApplication [-SearchString <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADApplication -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADApplication** cmdlet gets an Azure Active Directory application.

## EXAMPLES

### Example 1: Get an application by display name
```PowerShell
PS C:\>Get-AzureADApplication -Filter "DisplayName eq 'TestName'"

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
3ddd22e7-a150-4bb3-b100-e410dea1cb84 36ee4c6c-0812-40a2-b820-b22ebd02bce3 TestName
```
This command gets an application by its display name.





### Example 2: Get an application by ID
```
PS C:\>Get-AzureADApplication -Filter "AppId eq 'ed192e92-84d4-4baf-997d-1e190a81f28e'"
```
This command gets an application by its ID.

Output:

    ObjectId                             AppId                                DisplayName
    --------                             -----                                -----------  
    ed192e92-84d4-4baf-997d-1e190a81f28e 36ee4c6c-0812-40a2-b820-b22ebd02bce3 MyNewApp

## PARAMETERS

### -ObjectId
Specifies the ID of an application in Azure Active Directory.

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

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies a variable in which to store an information event message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[New-AzureADApplication](./New-AzureADApplication.md)  
[Remove-AzureADApplication](./Remove-AzureADApplication.md)  
[Set-AzureADApplication](./Set-AzureADApplication.md)




