---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSApplicationKey

## SYNOPSIS
Adds a new key to an application.

## SYNTAX

```
New-AzureADMSApplicationKey -ObjectId <String> -KeyCredential <KeyCredential>
 [-PasswordCredential <PasswordCredential>] -Proof <String> [<CommonParameters>]
```

## DESCRIPTION
Adds a new key to an application.

## EXAMPLES

### Example 1: Add a key credential to an application
```
PS C:\>New-AzureADMSApplicationKey -ObjectId 14a3f1ac-46a7-4d00-b1ca-0b2b84f033c2 -KeyCredential @{ key=[System.Convert]::FromBase64String("{base64cert}") } -PasswordCredential @{ displayname = "mypassword" } -Proof "{token}"
```

This command adds a key credential the specified application.

## PARAMETERS

### -KeyCredential
The application key credential to add.

NOTES: keyId value should be null.

```yaml
Type: KeyCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
The application password credential to add.

NOTES: keyId value should be null.

```yaml
Type: PasswordCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Proof
A signed JWT token used as a proof of possession of the existing keys

```yaml
Type: String
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
### Microsoft.Open.MSGraph.Model.KeyCredential
### Microsoft.Open.MSGraph.Model.PasswordCredential
## OUTPUTS

### Microsoft.Open.MSGraph.Model.KeyCredential
## NOTES

## RELATED LINKS

[Remove-AzureADMSApplicationKey]()

