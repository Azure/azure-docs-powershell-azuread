---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: EAD7BC01-298D-427D-A0AF-5610021D1BE8
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationPasswordCredential

## SYNOPSIS
Removes a password credential from an application.

## SYNTAX

```
Remove-AzureADApplicationPasswordCredential -ObjectId <String> -KeyId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADApplicationPasswordCredential** cmdlet removes a password credential from an application in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove an application password credential
```
PS C:\> $AppID = (Get-AzureADApplication -Top 1).objectId
PS C:\> $KeyIDs = Get-AzureADApplicationPasswordCredential -ObjectId $AppId
PS C:\> Remove-AzureADApplicationPasswordCredential -ObjectId $AppId -KeyId $KeyIds[0].KeyId
```

The first command gets the ID of an application by using the [Get-AzureADApplication](./Get-AzureADApplication.md) cmdlet, and then stores it in the $AppID variable.

The second command gets the password credential for the application identified by $AppID by using the [Get-AzureADApplicationPasswordCredential](./ Get-AzureADApplicationPasswordCredential.md) cmdlet. 
The command stores it in the $KeyId variable.

The final command removes the application password credential for the application identified by $AppID.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

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
Specifies an information variable.

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

### -KeyId
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID of the application in Azure AD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureADApplication](./Get-AzureADApplication.md)

[Get-AzureADApplicationPasswordCredential](./Get-AzureADApplicationPasswordCredential.md)

[Remove-AzureADApplicationPasswordCredential](./Remove-AzureADApplicationPasswordCredential.md)
