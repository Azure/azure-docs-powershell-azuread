---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Set-GovernanceRoleAssignmentRequest

## SYNOPSIS
Update a role assignment request

## SYNTAX

```
Set-GovernanceRoleAssignmentRequest [-AssignmentState <String>] [-Decision <String>] -Id <String>
 -ProviderId <String> [-Reason <String>] [-Schedule <GovernanceSchedule>] [<CommonParameters>]
```

## DESCRIPTION
Update a role assignment request

## EXAMPLES

### Example 1
```
PS C:\> Set-GovernanceRoleAssignmentRequest -ProviderId AzureResources -Id 8d28fcb3-1373-4810-8e84-75adea9a18be -Reason "{'RequestorReason':'test','AdminReason':'gg'}" -Decision "AdminDenied"
```

Update a role assignment request by setting to denied

## PARAMETERS

### -AssignmentState
The state of assignment, and the values can be Eligible or Active.
For decision of AdminApproved, it is required.

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

### -Decision
The administrator decision of the role assignment request.
The value should be updated as AdminApproved or AdminDenied.

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
The unique identifier of the specific role assignment request

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

### -ProviderId
The unique identifier of the specific provider

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

### -Reason
The reason provided by the administrator for his decision.

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

### -Schedule
The schedule of the role assignment request.
For status of AdminApproved, it is required.

```yaml
Type: GovernanceSchedule
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
