
# Azure AD cmdlets for working with extension attributes

## About extension attributes

Extension attributes offer a convenient way to extend your Azure AD directory with new attributes that you can use to store attribute values for objects in your directory. You can attach an extension attribute to the following object types:

+ users
+ groups
+ tenant details
+ devices
+ applications
+ service principals

Extension properties are registered on an Application object within the developer’s directory. After the application has been consented to by a user or an admin in the developer’s directory, the property is added to the target directory type and becomes immediately accessible in the developer’s directory. For a multi-tenant application, when the application is granted consent by a user or an admin in another organization, the extension properties become immediately accessible on the target directory type in the other organization’s directory.

If an organization consents to “read only” permissions for an application with registered extensions, the properties will still become accessible in the other organization’s directory. Additionally, extension properties are accessible by any consented application in an organization, not just for the application to which they are registered. Other consented applications in that organization can read or write values for the new extension property if they have sufficient permissions.

If the application is deleted or consent is removed in the other organization’s directory, the extension property becomes inaccessible on the target directory object. If the extension is deleted by the application, it also becomes inaccessible on the target directory object. If a multi-tenant application adds additional extension properties after consent was granted, these properties become immediately accessible in the other organization’s directory.

>Note: If an extension property’s value is set on an object and that property becomes inaccessible in that object’s directory, the property still counts against that object’s limit of 100 extension property values. The only way to remove the property value from consideration once it has been set is to explicitly set it to null. You cannot do this if the extension property is inaccessible.

You can read more about extension properties in [this article.](https://msdn.microsoft.com/en-us/library/azure/ad/graph/howto/azure-ad-graph-api-directory-schema-extensions)

## Examples

In these examples we'll be using a user object and work with extension properties. We'll first find the ObjectId of the user so we can easily refer to it later:

```powershell 
$UserId = (Get-AzureADUser -Searchstring <UPN of the user we're working with>).ObjectId 
```

### Get all property values of a user
```powershell 
(Get-AzureADUser -ObjectId $Userid).ToJson
```

### Get a user and show all extension properties
```powershell 
Get-AzureADUser -ObjectId $UserID | Select -ExpandProperty ExtensionProperty
```

This cmdlet returns all extension properties of a user with their current values:

```powershell 
Key                                                                   Value
---                                                                   -----
odata.metadata                                                        https://graph.windows.net/85b5ff1e-0402-400c-9e3c-0f9e965325d1/$metad...
odata.type                                                            Microsoft.DirectoryServices.User
thumbnailPhoto@odata.mediaContentType                                 image/Jpeg
extension_e5e29b8a85d941eab8d12162bd004528_extensionAttribute13       Test 
```

### Retrieve a the value of a specific extension property for a user

```powershell 
(Get-AzureADUserExtension -ObjectId $UserId).get_item("extension_e5e29b8a85d941eab8d12162bd004528_wWWHomePage")
```

### Retrieve all extension properties that are defined in your tenant

```powershell 
Get-AzureADApplication | Get-AzureADApplicationExtensionProperty 
```

### Create a new extension property

Extension properties are always created for a specific application. If you just want to add generic properties to your directory, you can create a placeholder application:

```powershell 
$MyApp = (New-AzureADApplication -DisplayName "My Properties Bag" -IdentifierUris "https://dummy").ObjectId 
```

Note that you need to create a service principal for this application in your directory as well, so you can create a new extension property:

```powershell 
New-AzureADServicePrincipal -AppId (Get-AzureADApplication -SearchString "My Properties Bag").AppId 
```

Now we can use this application to create a new extension property:

```powershell 
New-AzureADApplicationExtensionProperty -ObjectId $MyApp -Name "MyNewProperty" -DataType "String" -TargetObjects "User" 
```

When the cmdlet completes successfully it returns the new extension attribute object:

```powershell
ObjectId                             Name                                                     TargetObjects
--------                             ----                                                     -------------
91ec8ae5-6813-4453-afd7-31680a484892 extension_0380f0f700c040b5aa577c9268940b53_MyNewProperty {User}
```

>Note that the Name of the new property is generated from the format "Extension_" + <objectID of your placeholder application> + "_" + <the name of your new property>. The exact value of the name will therefore be different for different applications you create.
>Note that you can assign a property to more than one object type. In our example we only used one TargetObject, "User", but you could also have specified "User","Group", this would assign the object to both user and group objects.

### Setting values for extension properties

Using the extension property we used in the previous example, we can now assign a value to it:

```powershell 
Set-AzureADUserExtension -ObjectId $UserId -ExtensionName "extension_0380f0f700c040b5aa577c9268940b53_MyNewProperty" -ExtensionValue "MyNewValue" 
```

### Retrieving all extension attributes that are defined for your application

You can retrieve the list of extension attributes that have been defined for your application:

```powershell 
Get-AzureADApplicationExtensionProperty -ObjectId (Get-AzureADApplication -SearchString "My Properties Bag").ObjectId 
```

This cmdlet returns the list of extension properties in your application:

```powershell
ObjectId                             Name                                                      TargetObjects
--------                             ----                                                      -------------

91ec8ae5-6813-4453-afd7-31680a484892 extension_0380f0f700c040b5aa577c9268940b53_MyNewProperty  {User}
```
### Deleting extension properties

If you no longer need an extension property, you can delete it:

```powershell 
Remove-AzureADApplicationExtensionProperty -ObjectId (Get-AzureADApplication -SearchString "My Properties Bag").ObjectID -ExtensionPropertyId 91ec8ae5-6813-4453-afd7-31680a484892 
```
