---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 3C941FE3-032E-4160-8693-F68165A6E36C
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Convert-MsolFederatedUser

## SYNOPSIS
Updates a user in a domain that was recently converted from single sign-on.

## SYNTAX

```
Convert-MsolFederatedUser -UserPrincipalName <String> [-NewPassword <String>] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convert-MsolFederatedUser** cmdlet updates a user in a domain that was recently converted from single sign-on to standard authentication type.
Single sign-on is also known as identity federation.
A new password must be provided for the user.

## EXAMPLES

### Example 1: Convert a federated user
```
PS C:\> Convert-MsolFederatedUser -UserPrincipalName "pattifuller@contoso.com"
```

This command converts a federated user into a standard user.

## PARAMETERS

### -NewPassword
Specifies the new password of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Specifies the Azure Active Directory user ID for the user to convert.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
