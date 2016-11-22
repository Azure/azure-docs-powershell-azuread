---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationExtensionProperty

## SYNOPSIS
Get group extension properties

## SYNTAX

```
Get-AzureADApplicationExtensionProperty -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve the extension properties of an application
```
$AppObjectId = (Get-AzureADApplication -top 1).objectId
Get-AzureADApplicationExtensionProperty -ObjectId $AppObjectId

Output:

ObjectId                             Name                                                    TargetObjects
--------                             ----                                                    -------------
344ed560-f8e7-410e-ab9f-c795a7df5c36 extension_36ee4c6c081240a2b820b22ebd02bce3_NewAttribute {Group}
```

## PARAMETERS

### -ObjectId
The unique idenfier of an application in Azure Active Directory

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

