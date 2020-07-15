---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADApplicationSignInSummary

## SYNOPSIS
Get signin summary by last number of days

## SYNTAX

```
Get-AzureADApplicationSignInSummary -Days <Int32> [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADApplicationSignInSummary cmdlet gets sign in summaries for the last 7 or 30 days.

## EXAMPLES

### Example 1: Get sign in summary by application for the last week
```
PS C:\>Get-AzureADApplicationSignInSummary -Days 7 -Filter "appDisplayName eq 'Graph Explorer'"
```

This command gets a summary of all sign ins to Graph Explorer for the last 7 days.

### Example 2: Get sign in summaries for the last month
```
PS C:\>Get-AzureADApplicationSignInSummary -Days 30
```

This command gets summaries for all sign ins from the past 30 days.

## PARAMETERS

### -Days
Number of past days summary will contain.
Valid values are 7 and 30

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
{{ Fill Filter Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
{{ Fill Top Description }}

```yaml
Type: Int32
Parameter Sets: (All)
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

## OUTPUTS

### Microsoft.Online.Administration.GetApplicationSignInSummaryObjectsResponse
## NOTES
## RELATED LINKS
