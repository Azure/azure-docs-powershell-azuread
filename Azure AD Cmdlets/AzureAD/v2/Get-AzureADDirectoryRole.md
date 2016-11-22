---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDirectoryRole

## SYNOPSIS
Retrieves a specific directory role from Azure Active Directory

## SYNTAX

```
Get-AzureADDirectoryRole -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve a directory role
```
$Roles = Get-AzureADDirectoryRole
Get-AzureADDirectoryRole -ObjectId $Roles[0].ObjectId

Output:

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
019ea7a2-1613-47c9-81cb-20ba35b1ae48 Company Administrator              Company Administrator role has full access to perform any operation in the company scope.
```

### Retrieve all Roles from the directory
```
Get-AzureADDirectoryRole

Output:

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
019ea7a2-1613-47c9-81cb-20ba35b1ae48 Company Administrator              Company Administrator role has full access to perform any operation in the company scope.
2b3a80bc-51a4-476d-8e09-cd8b6cdde5ea Directory Writers                  Allows access read tasks and a subset of write tasks in the directory.
526b7173-5a6e-49dc-88ec-b677a9093709 User Account Administrator         User Account Administrator has access to perform common user management related tasks.
542f5aef-b23f-4e34-a838-6f2b9205b3d6 Directory Synchronization Accounts Directory Synchronization Accounts
68239fa3-6b01-4396-aeb4-6af38a1b6abf Directory Readers                  Allows access to various read only tasks in the directory.
8c6a5c45-e93e-4f2b-81be-b57ad4c43ddd Privileged Role Administrator      Privileged Role Administrator has access to perform common role management related tasks.
8f8a1cf4-d535-4ccd-8552-7267c7ee0a88 Helpdesk Administrator             Helpdesk Administrator has access to perform common helpdesk related tasks.
b89a48d4-7595-48d0-bb36-69fe4b220668 Device Administrators              Device Administrators
d96eb2b3-0970-4827-8f26-6008efd86511 Security Administrator             Security Administrator allows ability to read and manage security configuration and reports.
```

## PARAMETERS

### -ObjectId
The unique identifier of a directory role in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

