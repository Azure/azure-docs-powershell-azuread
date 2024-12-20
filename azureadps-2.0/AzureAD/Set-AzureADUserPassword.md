---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADUserPassword

## SYNOPSIS
Sets the password of a user.

## SYNTAX

```
Set-AzureADUserPassword -ObjectId <String> -Password <SecureString> [-ForceChangePasswordNextLogin <Boolean>]
 [-EnforceChangePasswordPolicy <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADUserPassword cmdlet sets the password for a user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Set a user's password
```
PS C:\>Set-AzureADUserPassword -ObjectId  "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -Password $password
```

This command sets the specified user's password.

## PARAMETERS

### -EnforceChangePasswordPolicy
If set to true, force the user to change their password

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

### -ForceChangePasswordNextLogin
Forces a user to change their password during their next log in.

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

### -ObjectId
Specifies the ID of an object.

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

### -Password
Specifies the password.

```yaml
Type: SecureString
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
