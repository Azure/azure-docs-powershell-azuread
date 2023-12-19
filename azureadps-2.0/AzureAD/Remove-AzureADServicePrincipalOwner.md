---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADServicePrincipalOwner

## SYNOPSIS
Removes an owner from a service principal.

## SYNTAX

```
Remove-AzureADServicePrincipalOwner -ObjectId <String> -OwnerId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADServicePrincipalOwner cmdlet removes an owner from a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> $ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> $OwnerId = (Get-AzureADServicePrincipalOwner -ObjectID $ServicePrincipalId -Top 1).ObjectId
PS C:\> Remove-AzureADServicePrincipalOwner -ObjectID $ServicePrincipalId -OwnerID $OwnerId
```

The first command gets the ID of the service principal and stores it in the $ServicePrincipalId variable.

The second command gets the ID of one owner of the specified service principal and stores it in the $OwnerId variable.

The third command removes the owner identified by $OwnerId of the service principal identified by $ServicePrincipalId.

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
Specifies the ID of a service principal.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

See the [migration guide for Remove-AzureADServicePrincipalOwner](./migrate/Remove-AzureADServicePrincipalOwner.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS

[Add-AzureADServicePrincipalOwner](Add-AzureADServicePrincipalOwner.md)

[Get-AzureADServicePrincipalOwner](Get-AzureADServicePrincipalOwner.md)

