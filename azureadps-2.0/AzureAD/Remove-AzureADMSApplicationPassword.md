---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSApplicationPassword

## SYNOPSIS
Remove a password from an application.

## SYNTAX

```
Remove-AzureADMSApplicationPassword -ObjectId <String> [-KeyId <String>] [<CommonParameters>]
```

## DESCRIPTION
Remove a password from an application.

## EXAMPLES

### Example 1: Removes a password from an application
```
PS C:\>Remove-AzureADMSApplicationPassWord -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -KeyId aaaaaaaa-0b0b-1c1c-2d2d-333333333333
```

This command remove the specified password from the specified application.

## PARAMETERS

### -ObjectId
The unique identifier of the object specific Azure Active Directory object

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

### -KeyId
The unique identifier for the key.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADMSApplicationPassword](New-AzureADMSApplicationPassword.md)
