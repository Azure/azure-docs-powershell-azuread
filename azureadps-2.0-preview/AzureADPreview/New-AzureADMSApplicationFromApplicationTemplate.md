---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSApplicationFromApplicationTemplate

## SYNOPSIS
Instantiates an application

## SYNTAX

```
New-AzureADMSApplicationFromApplicationTemplate -Id <String> -DisplayName <ApplicationTemplateDisplayName>
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows users to create application from application template

## EXAMPLES

### 1. Creates an application from application template
```
PS C:\> $instantiated_app = New-AzureADMSApplicationTemplate -Id  e8b7b394-057d-4203-a93a-1879c28ece38 -DisplayName bugzilla-copy1
```

This command instantiates a new application based on application template referenced by the id.

## PARAMETERS

### -Id
The unique identifier of an object in Azure Active Directory

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

### -DisplayName
Application template display name

```yaml
Type: ApplicationTemplateDisplayName
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

## OUTPUTS

### Microsoft.Online.Administration.ApplicationTemplateCopy
## NOTES
## RELATED LINKS
