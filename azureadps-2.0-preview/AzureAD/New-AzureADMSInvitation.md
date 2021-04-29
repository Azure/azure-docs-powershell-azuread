---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSInvitation

## SYNOPSIS
This cmdlet is used to invite a new external user to your directory

## SYNTAX

```
New-AzureADMSInvitation [-InvitedUserDisplayName <String>] -InvitedUserEmailAddress <String>
 [-SendInvitationMessage <Boolean>] -InviteRedirectUrl <String> [-InvitedUser <User>]
 [-InvitedUserMessageInfo <InvitedUserMessageInfo>] [-InvitedUserType <String>] [-ResetRedemption <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to invite a new external user to your directory.

## EXAMPLES

### Invite a new external user to your directory
```
New-AzureADMSInvitation -InvitedUserEmailAddress someexternaluser@externaldomain.com -SendInvitationMessage $True -InviteRedirectUrl "http://myapps.onmicrosoft.com"
```

Using the cmdlet in this example, an email is sent to the user who's email address is in the -InvitedUserEmailAddress parameter.
When the user accepts the invitation, they are forwarded to the url as specified in the -InviteRedirectUrl parameter

### Reset a Redemption for an external user
```
PS C:\> New-AzureADMSInvitation -InvitedUserEmailAddress someexternaluser@externaldomain.com -ResetRedemption $true -InvitedUser $user -InviteRedirectUrl "http://myapps.onmicrosoft.com"
```

In this example we show how an admin can reset the redemption for an external user in the -InvitedUser parameter.
They need to passed the switch -ResetRedemption as true.
Once reset, External user will have to re-redeem the invitation to continue to access the resources.

## PARAMETERS

### -InvitedUserDisplayName
The display name of the user as it will appear in your directory

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

### -InvitedUserEmailAddress
The Email address to which the invitation is sent

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

### -InvitedUserMessageInfo
Addition information to specify how the invitation message is sent

```yaml
Type: InvitedUserMessageInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InvitedUser
An existing user object in the directory that you want to add or update the B2B credentials for.

```yaml
Type: User
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InvitedUserType
The userType of the user being invited.
By default, this is Guest.
You can invite as Member if you're are company administrator.

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

### -InviteRedirectUrl
The URL to which the invited user is forwarded after accepting the invitation

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

### -SendInvitationMessage
A Boolean parameter that indicates whether or not an invitation message will be sent to the invited user.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetRedemption
Indicates whether the invite redemption on an existing external user should be removed so the user can re-redeem the account. 
By default, this is false and should only be set to true when passing in a valid external user to the InvitedUser property.

```yaml
Type: Boolean
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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
