---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSIdentityProvider

## SYNOPSIS
This cmdlet is used to update the properties of an existing identity provider configured in the directory.

## SYNTAX

```
Set-AzureADMSIdentityProvider -Id <String> [-Type <String>] [-Name <String>] [-ClientId <String>]
 [-ClientSecret <String>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet can be used to update the properties of an existing identity provider.
The type of the identity provider cannot be modified.

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADMSIdentityProvider -Id LinkedIn-OAUTH -ClientId NewClientId -ClientSecret NewClientSecret
```

This example updates the client ID and client secret for the specified identity provider.

## PARAMETERS

### -ClientId
The client ID for the application.
This is the client ID obtained when registering the application with the identity provider.

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

### -ClientSecret
The client secret for the application.
This is the client secret obtained when registering the application with the identity provider.

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

### -Id
The unique identifier for an identity provider.

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

### -Name
The display name of the identity provider.

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

### -Type
{{Fill Type Description}}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
