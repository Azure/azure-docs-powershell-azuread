---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADMSApplicationPassword

## SYNOPSIS
Adds a strong password to an application.

## SYNTAX

```
New-AzureADMSApplicationPassword -ObjectId <String> -PasswordCredential <PasswordCredential>
 [<CommonParameters>]
```

## DESCRIPTION
Adds a strong password to an application.

## EXAMPLES

### Example 1: Add a password to an application
```
PS C:\>New-AzureADMSApplicationPassword -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -PasswordCredential @{ displayname = "mypassword" }

          CustomKeyIdentifier :
          EndDateTime         : 10/28/2021 3:57:37 PM
          DisplayName         :
          KeyId               : aaaaaaaa-0b0b-1c1c-2d2d-333333333333
          StartDateTime       : 10/28/2019 3:57:37 PM
          SecretText          : EQ:A-s45?Rt9/3Bp?7]-7__IO]3AG09E
          Hint                : EQ:
```

This command adds a password to the specified application.

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

### -PasswordCredential
Represents a password credential associated with an application or a service principal.

```yaml
Type: PasswordCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
### Microsoft.Open.MSGraph.Model.PasswordCredential
## OUTPUTS

### Microsoft.Open.MSGraph.Model.PasswordCredential
## NOTES

## RELATED LINKS

[Remove-AzureADMSApplicationPassword]()
