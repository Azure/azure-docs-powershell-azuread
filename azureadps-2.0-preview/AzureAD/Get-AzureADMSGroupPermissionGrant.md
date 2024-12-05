---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSGroupPermissionGrant

## SYNOPSIS
Retrieves a list of permission grants that have been consented for this group.

## SYNTAX

```
Get-AzureADMSGroupPermissionGrant -Id <String> [<CommonParameters>]
```

## DESCRIPTION
Retrieves a list of permission grants that have been consented for this group.

## EXAMPLES

### Example 1: List existing permission grants for the group. .
```
List exisiting permission grants for the group.
		
		Get-AzureADMSGroupPermissionGrant -Id "4823e767eca44858aed244154009b764" 

		Id             : vsMaSY2k_E7761KhRqpx7OGFvAwvdZnJM1s7Iqkt4PU
		ClientId       : 00001111-aaaa-2222-bbbb-3333cccc4444
		ClientAppId    : 11112222-bbbb-3333-cccc-4444dddd5555
		ResourceAppId  : 00000003-0000-0000-c000-000000000000
		PermissionType : Application
		Permission     : Member.Read.Group
```

## PARAMETERS

### -Id
The unique identifier of group.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.GetMSGroupPermissionGrantsResponse
## NOTES

## RELATED LINKS
