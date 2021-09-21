---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSServicePrincipal

## SYNOPSIS
Gets a service principal.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSServicePrincipal [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [-Select <String>]
 [<CommonParameters>]
```

### GetVague
```
Get-AzureADMSServicePrincipal [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSServicePrincipal -Id <String> [-All <Boolean>] [-Select <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSServicePrincipal cmdlet gets a service principal in Azure Active Directory (Azure AD).

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSServicePrincipal

Id                                 : 055aa618-7c74-40ee-b278-75545562c3d6
ObjectId                           :
DeletionTimestamp                  :
AccountEnabled                     : true
AppId                              : 6ff5f225-c1d3-46cc-b89e-39e679ff746f
AppDisplayName                     : App Name
ApplicationTemplateId              :
AppRoleAssignmentRequired          : False
CustomSecurityAttributes           :
DisplayName                        : App Name
ErrorUrl                           :
LogoutUrl                          :
Homepage                           :
IsManagementRestricted             :
SamlMetadataUrl                    :
MicrosoftFirstParty                :
PublisherName                      : Microsoft Services
PreferredTokenSigningKeyThumbprint :
ReplyUrls                          : {}
ServicePrincipalNames              : {6ff5f225-c1d3-46cc-b89e-39e679ff746f}
Tags                               : {}
KeyCredentials                     : {}
PasswordCredentials                : {}
```

Get all service principals from the directory

### Example 2
```powershell
PS C:\> $sp = Get-AzureADMSServicePrincipal -Id 4a7c15df-ac88-44f3-84c6-fd0812701f29
```

Get a service principal by ID

### Example 3
```powershell
PS C:\> $ServicePrincipalId = (Get-AzureADMSServicePrincipal -Top 1).Id
PS C:\> Get-AzureADMSServicePrincipal $ServicePrincipalId
```

The first command gets the ID of a service principal by using the Get-AzureADMSServicePrincipal cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets the service principal identified by $ServicePrincipalId.

### Example 4
```powershell
PS C:\> Get-AzureADMSServicePrincipal -Select CustomSecurityAttributes
Get-AzureADMSServicePrincipal -Id 7d194b0c-bf17-40ff-9f7f-4b671de8dc20  -Select "CustomSecurityAttributes, Id"
```

List custom security attribute assignments for an application (service principal)

## PARAMETERS

### -All
If true, return all serviceprincipal objects.
If false, return the number of objects specified by the Top parameter

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

### -Filter
Specifies an oData v3.0 filter statement.
This parameter controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
Specifies the ID of a service principal in Azure AD.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Select
Specifies the properties to be returned on the object.

```yaml
Type: String
Parameter Sets: GetQuery, GetById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
