---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSApplication

## SYNOPSIS
Retrieves the list of applications within the organization.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSApplication [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADMSApplication [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSApplication -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves the list of applications within the organization.
With an ObjectId argument, it can retrieve the properties of the application object associated with the ObjectId.

## EXAMPLES

### Example 1: Get an application by display name
```
PS C:\>Get-AzureADMSApplication -Filter "DisplayName eq 'My App'"

          Id                        : ba4a97a7-3815-4752-bf4c-f1c0cccfff6a
          OdataType                 :
          Api                       : class ApiApplication {
          AcceptMappedClaims:
          KnownClientApplications:
          PreAuthorizedApplications:
          RequestedAccessTokenVersion: 2
          Oauth2PermissionScopes:
          System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PermissionScope]
          }

          AppId                     : 807dd73f-8451-4cfa-b3bc-52ac3fd95330
          AppRoles                  : {}
          IsDeviceOnlyAuthSupported :
          IsFallbackPublicClient    :
          IdentifierUris            : {}
          DeletedDateTime           :
          DisplayName               : My App
          Info                      : class InformationalUrl {
          TermsOfServiceUrl:
          MarketingUrl:
          PrivacyStatementUrl:
          SupportUrl:
          LogoUrl:
          }

          KeyCredentials            : {}
          OptionalClaims            :
          ParentalControlSettings   : class ParentalControlSettings {
          CountriesBlockedForMinors: System.Collections.Generic.List`1[System.String]
          LegalAgeGroupRule: Allow
          }

          PasswordCredentials       : {}
          PublicClientApplication   :
          RequiredResourceAccess    : {}
          SignInAudience            : AzureADandPersonalMicrosoftAccount
          Tags                      : {}
          TokenEncryptionKeyId      :
          Web                       : class WebApplication {
          LogoutUrl:
          Oauth2AllowImplicitFlow:
          RedirectUris: System.Collections.Generic.List`1[System.String]
          ImplicitGrantSettings: class ImplicitGrantSettings {
          EnableIdTokenIssuance: False
          EnableAccessTokenIssuance: False
          }

          }
```

This command gets an application by its display name.

### Example 2: Get an application by ID
```
PS C:\>Get-AzureADMSApplication -Filter "AppId eq 'ed192e92-84d4-4baf-997d-1e190a81f28e'"
```

This command gets an application by its ID.

Output:

Id                        : ba4a97a7-3815-4752-bf4c-f1c0cccfff6a
            OdataType                 :
            Api                       : class ApiApplication {
            AcceptMappedClaims:
            KnownClientApplications:
            PreAuthorizedApplications:
            RequestedAccessTokenVersion: 2
            Oauth2PermissionScopes:
            System.Collections.Generic.List\`1\[Microsoft.Open.MSGraph.Model.PermissionScope\]
            }

            AppId                     : 807dd73f-8451-4cfa-b3bc-52ac3fd95330
            AppRoles                  : {}
            IsDeviceOnlyAuthSupported :
            IsFallbackPublicClient    :
            IdentifierUris            : {}
            DeletedDateTime           :
            DisplayName               : My App
            Info                      : class InformationalUrl {
            TermsOfServiceUrl:
            MarketingUrl:
            PrivacyStatementUrl:
            SupportUrl:
            LogoUrl:
            }

            KeyCredentials            : {}
            OptionalClaims            :
            ParentalControlSettings   : class ParentalControlSettings {
            CountriesBlockedForMinors: System.Collections.Generic.List\`1\[System.String\]
            LegalAgeGroupRule: Allow
            }

            PasswordCredentials       : {}
            PublicClientApplication   :
            RequiredResourceAccess    : {}
            SignInAudience            : AzureADandPersonalMicrosoftAccount
            Tags                      : {}
            TokenEncryptionKeyId      :
            Web                       : class WebApplication {
            LogoutUrl:
            Oauth2AllowImplicitFlow:
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            ImplicitGrantSettings: class ImplicitGrantSettings {
            EnableIdTokenIssuance: False
            EnableAccessTokenIssuance: False
            }

            }

### Example 3: Retrieve an application by identifierUris
```
Get-AzureADMSApplication -Filter "identifierUris/any(uri:uri eq 'http://wingtips.wingtiptoysonline.com')"
```

### Example 4: Get an application by object ID
```
PS C:\>Get-AzureADMSApplication -ObjectId ffe886bc-e978-4002-829e-cf5b1e83d56a
```

This command gets an application by its object ID.

Output:

Id                        : f8bbcbe4-df80-4a6b-80c5-926e28e41407
            OdataType                 :
            AddIns                    : {}
            Api                       : class ApiApplication {
            AcceptMappedClaims:
            KnownClientApplications:
            PreAuthorizedApplications:
            RequestedAccessTokenVersion:
            Oauth2PermissionScopes:
            System.Collections.Generic.List\`1\[Microsoft.Open.MSGraph.Model.PermissionScope\]
            ResourceSpecificApplicationPermissions:
            }

            AppId                     : 18f78c92-365c-4fa0-9b6f-7e06fff27ffe
            ApplicationTemplateId     :
            AppRoles                  : {}
            GroupMembershipClaims     :
            IsDeviceOnlyAuthSupported :
            IsFallbackPublicClient    :
            IdentifierUris            : {}
            CreatedDateTime           :
            DeletedDateTime           :
            DisplayName               : my app
            Info                      : class InformationalUrl {
            TermsOfServiceUrl:
            MarketingUrl:
            PrivacyStatementUrl:
            SupportUrl:
            LogoUrl:
            }

            KeyCredentials            : {}
            OptionalClaims            :
            ParentalControlSettings   : class ParentalControlSettings {
            CountriesBlockedForMinors: System.Collections.Generic.List\`1\[System.String\]
            LegalAgeGroupRule: Allow
            }

            PasswordCredentials       : {}
            PublicClient              : class PublicClientApplication {
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            }

            PublisherDomain           :
            RequiredResourceAccess    : {}
            SignInAudience            : AzureADMyOrg
            Tags                      : {}
            TokenEncryptionKeyId      :
            Web                       : class WebApplication {
            HomePageUrl:
            LogoutUrl:
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            ImplicitGrantSettings: class ImplicitGrantSettings {
            EnableIdTokenIssuance: True
            EnableAccessTokenIssuance: False
            }

            }

### Example 5: Get the first 2 applications
```
PS C:\>Get-AzureADMSApplication -Top 2
```

This command gets the first 2 applications

Output:

Id                        : 121ce3aa-64cb-44f2-99e8-deb705caeddd
            OdataType                 :
            AddIns                    : {}
            Api                       : class ApiApplication {
            AcceptMappedClaims:
            KnownClientApplications:
            PreAuthorizedApplications:
            RequestedAccessTokenVersion: 2
            Oauth2PermissionScopes:
            System.Collections.Generic.List\`1\[Microsoft.Open.MSGraph.Model.PermissionScope\]
            ResourceSpecificApplicationPermissions:
            }

            AppId                     : a1293e4b-97ae-4f58-9eeb-d0ba5b4b821a
            ApplicationTemplateId     :
            AppRoles                  : {}
            GroupMembershipClaims     :
            IsDeviceOnlyAuthSupported :
            IsFallbackPublicClient    :
            IdentifierUris            : {}
            CreatedDateTime           :
            DeletedDateTime           :
            DisplayName               : My App
            Info                      : class InformationalUrl {
            TermsOfServiceUrl:
            MarketingUrl:
            PrivacyStatementUrl:
            SupportUrl:
            LogoUrl:
            }

            KeyCredentials            : {}
            OptionalClaims            :
            ParentalControlSettings   : class ParentalControlSettings {
            CountriesBlockedForMinors: System.Collections.Generic.List\`1\[System.String\]
            LegalAgeGroupRule: Allow
            }

            PasswordCredentials       : {}
            PublicClient              : class PublicClientApplication {
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            }

            PublisherDomain           :
            RequiredResourceAccess    : {}
            SignInAudience            : AzureADandPersonalMicrosoftAccount
            Tags                      : {}
            TokenEncryptionKeyId      :
            Web                       : class WebApplication {
            HomePageUrl:
            LogoutUrl:
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            ImplicitGrantSettings: class ImplicitGrantSettings {
            EnableIdTokenIssuance: False
            EnableAccessTokenIssuance: False
            }

            }


            Id                        : 14a3f1ac-46a7-4d00-b1ca-0b2b84f033c2
            OdataType                 :
            AddIns                    : {}
            Api                       : class ApiApplication {
            AcceptMappedClaims:
            KnownClientApplications:
            PreAuthorizedApplications:
            RequestedAccessTokenVersion: 2
            Oauth2PermissionScopes:
            System.Collections.Generic.List\`1\[Microsoft.Open.MSGraph.Model.PermissionScope\]
            ResourceSpecificApplicationPermissions:
            }

            AppId                     : 51546bbc-4233-42d3-a08e-c73a370f5d41
            ApplicationTemplateId     :
            AppRoles                  : {}
            GroupMembershipClaims     :
            IsDeviceOnlyAuthSupported :
            IsFallbackPublicClient    :
            IdentifierUris            : {}
            CreatedDateTime           :
            DeletedDateTime           :
            DisplayName               : My App
            Info                      : class InformationalUrl {
            TermsOfServiceUrl:
            MarketingUrl:
            PrivacyStatementUrl:
            SupportUrl:
            LogoUrl:
            }

            KeyCredentials            : {}
            OptionalClaims            :
            ParentalControlSettings   : class ParentalControlSettings {
            CountriesBlockedForMinors: System.Collections.Generic.List\`1\[System.String\]
            LegalAgeGroupRule: Allow
            }

            PasswordCredentials       : {}
            PublicClient              : class PublicClientApplication {
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            }

            PublisherDomain           :
            RequiredResourceAccess    : {}
            SignInAudience            : AzureADandPersonalMicrosoftAccount
            Tags                      : {}
            TokenEncryptionKeyId      :
            Web                       : class WebApplication {
            HomePageUrl:
            LogoutUrl:
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            ImplicitGrantSettings: class ImplicitGrantSettings {
            EnableIdTokenIssuance: False
            EnableAccessTokenIssuance: False
            }

            }

### Example 6: Retrieve a list of all applications
```
PS C:\>Get-AzureADMSApplication -All $true
```

### Example 5: Retrieve a list of all applications which have a display name that contains "asdfl"
```
PS C:\>Get-AzureADMSApplication -SearchString asdfl
```

This command gets a list of applications which have the specified display name

Output:

Id                        : 88da75d4-2cba-4c47-9a15-80a983228ad4
            OdataType                 :
            AddIns                    : {}
            Api                       : class ApiApplication {
            AcceptMappedClaims:
            KnownClientApplications:
            PreAuthorizedApplications:
            RequestedAccessTokenVersion: 2
            Oauth2PermissionScopes:
            System.Collections.Generic.List\`1\[Microsoft.Open.MSGraph.Model.PermissionScope\]
            ResourceSpecificApplicationPermissions:
            }

            AppId                     : 2cffc854-bbcf-404a-8bba-70d043534129
            ApplicationTemplateId     :
            AppRoles                  : {}
            GroupMembershipClaims     :
            IsDeviceOnlyAuthSupported :
            IsFallbackPublicClient    :
            IdentifierUris            : {}
            CreatedDateTime           : 10/24/2019 6:27:25 AM
            DeletedDateTime           :
            DisplayName               : asdflkj
            Info                      : class InformationalUrl {
            TermsOfServiceUrl:
            MarketingUrl:
            PrivacyStatementUrl:
            SupportUrl:
            LogoUrl:
            }

            KeyCredentials            : {}
            OptionalClaims            :
            ParentalControlSettings   : class ParentalControlSettings {
            CountriesBlockedForMinors: System.Collections.Generic.List\`1\[System.String\]
            LegalAgeGroupRule: Allow
            }

            PasswordCredentials       : {}
            PublicClient              : class PublicClientApplication {
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            }

            PublisherDomain           :
            RequiredResourceAccess    : {}
            SignInAudience            : AzureADandPersonalMicrosoftAccount
            Tags                      : {}
            TokenEncryptionKeyId      :
            Web                       : class WebApplication {
            HomePageUrl:
            LogoutUrl:
            RedirectUris: System.Collections.Generic.List\`1\[System.String\]
            ImplicitGrantSettings: class ImplicitGrantSettings {
            EnableIdTokenIssuance: False
            EnableAccessTokenIssuance: False
            }

            }

## PARAMETERS

### -ObjectId
Specifies the ID of an application in Azure Active Directory

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -All
If true, return all applications.
If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
Specifies an oData v3.0 filter statement.
This parameter controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Retrieve only those applications that satisfy the -SearchString value

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### bool?
### int?
### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.MsApplication
## NOTES

## RELATED LINKS

[New-AzureADMSApplication]()

[Remove-AzureADMSApplication]()

[Set-AzureADMSApplication]()

