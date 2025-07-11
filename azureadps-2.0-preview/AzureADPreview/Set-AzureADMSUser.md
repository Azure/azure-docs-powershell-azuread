---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSUser

## SYNOPSIS
Updates a user.

## SYNTAX

```
Set-AzureADMSUser -Id <String> [-DisplayName <String>] [-CustomSecurityAttributes <Object>]
 [-UserPrincipalName <String>] [<CommonParameters>]
```

## DESCRIPTION
Updates a user in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> $user = Get-AzureADMSUser -UserPrincipalName TestUser@example.com 
PS C:\> $user.DisplayName = 'YetAnotherTestUser' 
PS C:\> Set-AzureADMSUser -UserPrincipalName TestUser@example.com -Displayname $user.Displayname
```

Update a user.

### Example 2
```powershell
PS C:\> $attributes = @{
    Engineering = @{
        "@odata.type" = "#Microsoft.DirectoryServices.CustomSecurityAttributeValue"
        "Project@odata.type" = "#Collection(String)"
        Project = @("Baker","Cascade")
    }
} 
PS C:\> Set-AzureADMSUser -Id dbb22700-a7de-4372-ae78-0098ee60e55e -CustomSecurityAttributes $attributes
```

Assign a custom security attribute with a multi-string value to a user.

- Attribute set: `Engineering`
- Attribute: `Project`
- Attribute data type: Collection of Strings
- Attribute value: `("Baker","Cascade")`

### Example 3
```powershell
PS C:\> $attributesUpdate = @{
    Engineering = @{
        "@odata.type" = "#Microsoft.DirectoryServices.CustomSecurityAttributeValue"
        "Project@odata.type" = "#Collection(String)"
        Project = @("Alpine","Baker")
    }
}
PS C:\> Set-AzureADMSUser -Id dbb22700-a7de-4372-ae78-0098ee60e55e -CustomSecurityAttributes $attributes
```

Update a custom security attribute with a multi-string value for a user.

- Attribute set: `Engineering`
- Attribute: `Project`
- Attribute data type: Collection of Strings
- Attribute value: `("Alpine","Baker")`

## PARAMETERS

### -CustomSecurityAttributes
Custom security attributes for the user.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies the user's display name.

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
Specifies the ID of a user in Azure AD.

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

### -UserPrincipalName
Specifies the user principal name of a user in Azure AD.

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

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
