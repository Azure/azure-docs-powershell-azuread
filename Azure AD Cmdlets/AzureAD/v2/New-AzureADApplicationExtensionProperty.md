---
external help file: azuread.help.xml
online version: https://docs.microsoft.com/en-us/powershell/azuread/v2/new-azureadapplication
schema: 2.0.0
---

# New-AzureADApplicationExtensionProperty

## SYNOPSIS
Create application extension property

## SYNTAX

```
New-AzureADApplicationExtensionProperty -ObjectId <String> [-DataType <String>] [-Name <String>]
 [-TargetObjects <List`1[String]>]
```

## DESCRIPTION

## EXAMPLES

### Create a new application extension property
```
$AppId = (Get-AzureADApplication -Top 1).ObjectId
New-AzureADApplicationExtensionProperty -ObjectID $AppId -DataType "string" -Name "NewAttribute"

Output:

ObjectId                             Name                                                    TargetObjects
--------                             ----                                                    -------------
344ed560-f8e7-410e-ab9f-c795a7df5c36 extension_36ee4c6c081240a2b820b22ebd02bce3_NewAttribute {}
```

## PARAMETERS

### -ObjectId
The unique identifier of an application in Azure Active Directory

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

### -DataType
@{Text=}

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

### -Name
@{Text=}

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

### -TargetObjects
@{Text=}

```yaml
Type: List`1[String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

