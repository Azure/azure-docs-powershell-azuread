---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 186B4EE1-A85A-45C0-B480-ABB4FBEF9AE0
online version: 
schema: 2.0.0
---

# Get-AzureADDirectoryRoleTemplate

## SYNOPSIS
Gets directory role templates.

## SYNTAX

```
Get-AzureADDirectoryRoleTemplate [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDirectoryRoleTemplate** cmdlet gets directory role templates in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get role templates
```
PS C:\>Get-AzureADDirectoryRoleTemplate

ObjectId                             DisplayName                             Description
--------                             -----------                             -----------
729827e3-9c14-49f7-bb1b-9608f156bbb8 Helpdesk Administrator                  Helpdesk Administrator has access to perform common helpdesk related tasks.
f023fd81-a637-4b56-95fd-791ac0226033 Service Support Administrator           Service Support Administrator has access to perform common support tasks.
b0f54661-2d74-4c50-afa3-1ec803f12efe Billing Administrator                   Billing Administrator has access to perform common billing related tasks.
b5468a13-3945-4a40-b0b1-5d78c2676bbf Mailbox Administrator                   Allows access and management of users mailboxes.
4ba39ca4-527c-499a-b93d-d9b492c50246 Partner Tier1 Support                   Allows ability to perform tier1 support tasks.
e00e864a-17c5-4a4b-9c06-f5b95a8d5bd8 Partner Tier2 Support                   Allows ability to perform tier2 support tasks.
88d8e3e3-8f55-4a1e-953a-9b9898b8876b Directory Readers                       Allows access to various read only tasks in the directory.
29232cdf-9323-42fd-ade2-1d097af3e4de Exchange Service Administrator          Exchange Service Administrator.
75941009-915a-4869-abe7-691bff18279e Lync Service Administrator              Lync Service Administrator.
fe930be7-5e62-47db-91af-98c3a49a38b1 User Account Administrator              User Account Administrator has access to perform common user management related tasks.
9360feb5-f418-4baa-8175-e2a00bac4301 Directory Writers                       Allows access read tasks and a subset of write tasks in the directory.
62e90394-69f5-4237-9190-012177145e10 Company Administrator                   Company Administrator role has full access to perform any operation in the company scope.
a0b1b346-4d3e-4e8b-98f8-753987be4970 User                                    Every user is implicitly considered to be a member of the User Role.
d65e02d2-0214-4674-8e5d-766fb330e2c0 Email Verified User Creator             Allows creation of new email verified users.
eb1d8c34-acf5-460d-8424-c1f1a6fbdb85 AdHoc License Administrator             Allows access manage AdHoc license.
f28a1f50-f6e7-4571-818b-6a12f2af6b6c SharePoint Service Administrator        SharePoint Service Administrator.
d405c6df-0af8-4e3b-95e4-4d06e542189e Device Users                            Device Users
9f06204d-73c1-4d4c-880a-6edb90606fd8 Device Administrators                   Device Administrators
9c094953-4995-41c8-84c8-3ebb9b32c93f Device Join                             Device Join
c34f683f-4d5a-4403-affd-6615e00e3a7f Workplace Device Join                   Workplace Device Join
17315797-102d-40b4-93e0-432062caca18 Compliance Administrator                Compliance administrator.
d29b2b05-8046-44ba-8758-1e26182fcf32 Directory Synchronization Accounts      Directory Synchronization Accounts
2b499bcd-da44-4968-8aec-78e1674fa64d Device Managers                         Allows access to read and edit device properties.
9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3 Application Administrator               Application Administrator role has access to perform common application management related tasks.
cf1c38e5-3621-4004-a7cb-879624dced7c Application Developer                   Application Developer role has ability to create single-tenant applications.
5d6b6bb7-de71-4623-b4af-96380a352509 Security Reader                         Security Reader allows ability to read security information and reports.
194ae4cb-b126-40b2-bd5b-6091b380977d Security Administrator                  Security Administrator allows ability to read and manage security configuration and reports.
e8611ab8-c189-46e8-94e1-60213ab1f814 Privileged Role Administrator           Privileged Role Administrator has access to perform common role management related tasks.
3a2c62db-5318-420d-8d74-23affee5d9d5 Intune Service Administrator            Intune Service Administrator has full access in the Intune Service.
158c047a-c907-4556-b7ef-446551a6b5f7 Application Proxy Service Administrator Application Proxy Service Administrator has full access in the Application Proxy Service.
5c4f9dcd-47dc-4cf7-8c9a-9e4207cbfc91 Customer LockBox Access Approver        Customer LockBox Access Approver has approval access to user data requests.
44367163-eba1-44c3-98af-f5787879f96a CRM Service Administrator               CRM Service Administrator has full access in the CRM Service.
a9ea8996-122f-4c74-9520-8edcd192826c Power BI Service Administrator          Full access in the Power BI Service.
```

This command gets the role templates in Azure AD.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

