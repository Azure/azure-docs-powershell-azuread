---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: CF0916CC-7239-438D-87F7-BF39B733B77F
---

# Remove-MsolUser

## SYNOPSIS
Removes a user from Microsoft Azure Active Directory.

## SYNTAX

### RemoveUser__0 (Default)
```
Remove-MsolUser -ObjectId <Guid> [-RemoveFromRecycleBin] [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveUserByUpn__0
```
Remove-MsolUser [-RemoveFromRecycleBin] [-Force] -UserPrincipalName <String> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolUser cmdlet is used to remove a user from Microsoft Azure Active Directory.
This cmdlet will delete the user, their licenses, and any other associated data.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolUser -UserPrincipalName user@contoso.com

          None
```

Description

-----------

This command removes user@contoso.com from Microsoft Azure Active Directory. 
If the user has any licenses these will be removed as well. 
A confirmation prompt will be output to the screen to confirm the operation.

### -------------------------- EXAMPLE 2 --------------------------
```
Remove-MsolUser -UserPrincipalName user@contoso.com -force

          None
```

Description

-----------

This command removes user@contoso.com from Microsoft Azure Active Directory. 
If the user has any licenses these will be removed as well.

### -------------------------- EXAMPLE 3 --------------------------
```
Remove-MsolUser -UserPrincipalName user@contoso.com -RemoveFromRecycleBin

          None
```

Description

-----------

This command removes user@contoso.com from the Microsoft Azure Active Directory recycle bin.
A confirmation prompt will be output to the screen to confirm the operation. 
This command will permanently remove the user with no opportunity to recover the user.

## PARAMETERS

### -Force
Used to bypass onscreen confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
The object ID of the user to remove.

```yaml
Type: Guid
Parameter Sets: RemoveUser__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemoveFromRecycleBin
Used to permanently remove a deleted user from the recycle bin.
This operation, which can only be applied to deleted users, will permanently delete the user from Microsoft Azure Active Directory.
Once this operation has been completed, you will not be able to use the Restore-MsolUser command to recover the user.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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
The user ID of the user to remove.

```yaml
Type: String
Parameter Sets: RemoveUserByUpn__0
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


