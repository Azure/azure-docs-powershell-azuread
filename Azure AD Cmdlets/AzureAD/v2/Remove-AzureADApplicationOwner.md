---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 6B318FF5-2DD5-485A-A4BA-C2E9F7CA1DEC
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationOwner

## SYNOPSIS
Removes an owner from an application.

## SYNTAX

```
Remove-AzureADApplicationOwner -ObjectId <String> -OwnerId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADApplicationOwner** cmdlet removes an owner from an application in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove an owner from an application
```
PS C:\>Remove-AzureADApplicationOwner -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84" -OwnerId "c13dd34a-492b-4561-b171-40fcce2916c5"
```

This command removes the owner from the specified application.

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

### -ObjectId
Specifies the ID of an application in Azure AD.

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

### -OwnerId
Specifies the ID of the owner.

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

[Add-AzureADApplicationOwner](./Add-AzureADApplicationOwner.md)

[Get-AzureADApplicationOwner](./Get-AzureADApplicationOwner.md)
