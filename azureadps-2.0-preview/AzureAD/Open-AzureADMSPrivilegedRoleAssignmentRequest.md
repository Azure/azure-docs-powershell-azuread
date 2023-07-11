---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Open-AzureADMSPrivilegedRoleAssignmentRequest

## SYNOPSIS
Create a role assignment request

## SYNTAX

```
Open-AzureADMSPrivilegedRoleAssignmentRequest -ProviderId <String> -ResourceId <String>
 -RoleDefinitionId <String> -SubjectId <String> -Type <String> -AssignmentState <String>
 -Schedule <AzureADMSPrivilegedSchedule> [-Reason <String>] [<CommonParameters>]
```

## DESCRIPTION
Create a role assignment request

## EXAMPLES

### Example 1: Create an eligible role assignment request

```powershell
$schedule = New-Object Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedSchedule
$schedule.Type = "Once"
$schedule.StartDateTime = "2019-04-26T20:49:11.770Z"
$schedule.endDateTime = "2019-07-25T20:49:11.770Z"
Open-AzureADMSPrivilegedRoleAssignmentRequest -ProviderId AzureResources -Schedule $schedule -ResourceId "e5e7d29d-5465-45ac-885f-4716a5ee74b5" -RoleDefinitionId "9f8c1837-f885-4dfd-9a75-990f9222b21d" -SubjectId "a25004a3-eceb-4ad4-b4aa-9485356bc55b" -AssignmentState "Eligible" -Type "AdminAdd"
```

This example creates a role assignment request.

### Example 2: Activate an eligible role assignment for 4 hours

```powershell
$Duration = 4 # Number in Hours
$Date = Get-Date
$start = $Date.ToUniversalTime()
$end = $Date.AddHours($Duration).ToUniversalTime()

$schedule = New-Object Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedSchedule
$schedule.Type = 'Once'
$schedule.StartDateTime = $start.ToString('yyyy-MM-ddTHH:mm:ss.fffZ')
$schedule.endDateTime = $end.ToString('yyyy-MM-ddTHH:mm:ss.fffZ')

Open-AzureADMSPrivilegedRoleAssignmentRequest -ProviderId AzureResources -Schedule $schedule -ResourceId "e5e7d29d-5465-45ac-885f-4716a5ee74b5" -RoleDefinitionId "9f8c1837-f885-4dfd-9a75-990f9222b21d" -SubjectId "a25004a3-eceb-4ad4-b4aa-9485356bc55b" -AssignmentState "Active" -Type "UserAdd"
```

This example creates a role assignment request activating the Admin Role.

### Example 3: Deactivate a currently active role assignment

```powershell
$Duration = 0 # Disables the role immediately
$Date = Get-Date
$start = $Date.ToUniversalTime()
$end = $Date.AddHours($Duration).ToUniversalTime()

$schedule = New-Object Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedSchedule
$schedule.Type = 'Once'
$schedule.StartDateTime = $start.ToString('yyyy-MM-ddTHH:mm:ss.fffZ')
$schedule.endDateTime = $end.ToString('yyyy-MM-ddTHH:mm:ss.fffZ')

Open-AzureADMSPrivilegedRoleAssignmentRequest -ProviderId AzureResources -Schedule $schedule -ResourceId "e5e7d29d-5465-45ac-885f-4716a5ee74b5" -RoleDefinitionId "9f8c1837-f885-4dfd-9a75-990f9222b21d" -SubjectId "a25004a3-eceb-4ad4-b4aa-9485356bc55b" -AssignmentState "Active" -Type "UserRemove"
```

This example creates a role assignment request disabling the Admin Role.

## PARAMETERS

### -AssignmentState
The state of assignment.
The value can be Eligible and Active.
Required.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
The reason needs to be provided for the role assignment request for audit and review purpose.

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

### -ResourceId
The unique identifier of the specific resource

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
The ID of the role definition.
Required.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
The schedule of the role assignment request.
For request type of UserAdd, AdminAdd, AdminUpdate, and AdminExtend, it is required.

```yaml
Type: AzureADMSPrivilegedSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubjectId
The ID of the subject.
Required.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
The request type.
The value can be AdminAdd, UserAdd, AdminUpdate, AdminRemove, UserRemove, UserExtend, UserRenew, AdminRenew and AdminExtend.
Required.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

- [Assign Azure AD roles in Privileged Identity Management using Microsoft Graph PowerShell](/powershell/microsoftgraph/tutorial-pim?view=graph-powershell-1.0)
