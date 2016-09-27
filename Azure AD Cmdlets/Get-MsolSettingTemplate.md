---
external help file: AzureADHelpMSOL.xml
online version: 4955285a-6fe5-46e2-affc-8b1798ae8f2a
schema: 2.0.0
---

# Get-MsolSettingTemplate

## SYNOPSIS
Gets a directory setting template.

## SYNTAX

```
Get-MsolSettingTemplate -TemplateId <String>
```

## DESCRIPTION
The **Get-MsolSettingTemplate** cmdlet gets a directory setting template.

## EXAMPLES

### Example 1: Get a directory setting template
```
PS C:\>Get-MsolSettingTemplate -TemplateId "566F7EA7-7BF1-4F4A-AF23-A1B46DBD46D6"
```

This command gets a directory setting template with the specified template ID.

## PARAMETERS

### -TemplateId
Specifies the template ID associated with the directory setting template that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.SettingTemplate
This cmdlet returns a directory setting template that contains the following information: 

-- Id: The unique string ID of the directory setting template.
This value should be used when updating setting. 
-- DisplayName: The name of the setting template. 
-- Description: The description of the setting template. 
-- Values: The name value pair that describes setting template detail.

## NOTES

## RELATED LINKS

