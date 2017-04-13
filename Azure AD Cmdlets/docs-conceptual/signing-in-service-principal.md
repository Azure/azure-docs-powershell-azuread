
# Using a Service Principal to connect to a directory in PowerShell

This example describes how you can use a Service Principal to connect to your directory from within PowerShell. You would use this approach if you wanted to run an unattended script, as from Windows Scheduled tasks.

To enable this, we need to perform several steps. 

## Sign in to Azure AD PowerShell with an admin account

First, you need to sign in into a PowerShell session using an admin account:

```powershell
Connect-AzureAD
```

## Create a self signed certificate

We'll use a self signed certificate for this example, so let's create one. You'll want to replace the <password> string inthe below example with a password of your choice, this is the password that is used to create the certificate file.

```powershell
$pwd = "<password>"
$thumb = (New-SelfSignedCertificate -DnsName "drumkit.onmicrosoft.com" -CertStoreLocation "cert:\LocalMachine\My"  -KeyExportPolicy Exportable -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -NotAfter $notAfter).Thumbprint
$pwd = ConvertTo-SecureString -String $pwd -Force -AsPlainText
Export-PfxCertificate -cert "cert:\localmachine\my\$thumb" -FilePath c:\temp\examplecert.pfx -Password $pwd
```

## Load the certificate

Now that we have a certificate file, we'll need to load it so we can assign it to a new application we're creating:

```powershell
$cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate("C:\temp\examplecert.pfx", $pwd)
$keyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
```

## Create the Azure Active Directory Application

Next step is to create a new application and assign the certificate we created as a key credential:

```powershell 
$application = New-AzureADApplication -DisplayName "test123" -IdentifierUris "https://rodejo2177668"
New-AzureADApplicationKeyCredential -ObjectId $application.ObjectId -CustomKeyIdentifier "Test123" -Type AsymmetricX509Cert -Usage Verify -Value $keyValue
```

## Create the Service Principal and connect it to the Application

To use the application to sign in into your directory with PowerShell you'll need to create a new service principal for this application:

```powershell 
$sp=New-AzureADServicePrincipal -AppId $application.AppId 
```

## Give the Service Principal Reader access to the current tenant (Get-AzureADDirectoryRole)

We now have the ability to set the exact access rights this service principal has in your directory. In this example, we'll assign the access rights of the Directory Readers role in Azure AD:

```powershell 
Add-AzureADDirectoryRoleMember -ObjectId (Get-AzureADDirectoryRole | where-object {$_.DisplayName -eq "Directory Readers"}).Objectid -RefObjectId $sp.ObjectId 
```

This concludes the setup portion of the example. 

## Signing in into your tenant

We can now sign in to the directory using the new service principal. 
> Note: if you;re running all these commands in one script, as you probably would do when trying this out, please remember that Azure AD requires some time to sync all the information you just entered through all of its components. In that case, add a Sleep cmdlet call here, this will make the script processing pause for 5 seconds:

```powershell 
Sleep -s 5 
``` 
 
To sign in you will need to find the ObjectID of the tenant you want to sign in to:

```powershell
$tenant=Get-AzureADTenantDetail
```
Now you can sign in into your directory Azure AD PowerShell with your Service Principal and Certificate
```powershell
Connect-AzureAD -TenantId $tenant.ObjectId -ApplicationId  $Application.AppId -CertificateThumbprint $thumb
```
