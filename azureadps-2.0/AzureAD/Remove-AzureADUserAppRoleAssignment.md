---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADUserAppRoleAssignment

## SYNOPSIS
Removes a user application role assignment.

## SYNTAX

```
Remove-AzureADUserAppRoleAssignment -ObjectId <String> -AppRoleAssignmentId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADUserAppRoleAssignment cmdlet removes a user application role assignment in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> $appRoleAssignmentId = "AOpk4dbpHUiYomPPDlBfoglrwbCoExFLjTo8P-HhRC5"
$user = Get-AzureADUser -ObjectId "james.smith@example.com"

Remove-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -AppRoleAssignmentId $appRoleAssignmentId
```
Remove a single App Role Assignment with a known Id 

### Example 2
```powershell
PS C:\> $username = "james.smith@example.com"
$appname = "example-app"

$servicePrincipal = Get-AzureADServicePrincipal -Filter "Displayname eq '$appname'"
$user = Get-AzureADUser -ObjectId $username

Get-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId | Where-Object {( $_.ResourceId -eq $servicePrincipal.ObjectId ) -and ( $_.PrincipalId -eq $user.ObjectId ) -and ( $_.PrincipalType -eq "User")  | ForEach-Object -Process { Remove-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -AppRoleAssignmentId $_.ObjectId }
```
Remove all of a users App Role assignments for a a given AD Service Principle (Enterprise Application in Azure AD Interface). Please note this will only remove direct assignments to the user. Group assignments may also still be present for groups the user is in. 

## PARAMETERS

### -AppRoleAssignmentId
Specifies the ID of an application role assignment.

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

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID (as a UPN or ObjectId) of a user in Azure AD.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUserAppRoleAssignment]()

[New-AzureADUserAppRoleAssignment]()

