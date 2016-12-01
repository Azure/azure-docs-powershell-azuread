---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# New-AzureADMSInvitation

## SYNOPSIS
This cmdlet is used to invite a new external user to your directory

## SYNTAX

```
New-AzureADMSInvitation -InviteRedirectUrl <String> [-InvitedUserDisplayName <String>]
 -InvitedUserEmailAddress <String> [-InvitedUserMessageInfo <InvitedUserMessageInfo>]
 [-SendInvitationMessage <Boolean>]
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

## PARAMETERS

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

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES
Please note that this cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview we may still need to make changes to the cmdlet which could potentially cause unexpected effects.
We discourage customers from using this cmdlet in a production environment.

## RELATED LINKS

