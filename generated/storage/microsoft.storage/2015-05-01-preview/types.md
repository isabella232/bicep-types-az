# Microsoft.Storage @ 2015-05-01-preview

## Resource Microsoft.Storage/storageAccounts@2015-05-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-05-01-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: StorageAccountPropertiesCreateParameters
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.Storage/storageAccounts' (ReadOnly, DeployTimeConstant)

## StorageAccountPropertiesCreateParameters
### Properties
* **accountType**: 'Premium_LRS' | 'Standard_GRS' | 'Standard_LRS' | 'Standard_RAGRS' | 'Standard_ZRS'
* **creationTime**: string (ReadOnly)
* **customDomain**: CustomDomain (ReadOnly)
* **lastGeoFailoverTime**: string (ReadOnly)
* **primaryEndpoints**: Endpoints (ReadOnly)
* **primaryLocation**: string (ReadOnly)
* **provisioningState**: 'Creating' | 'ResolvingDNS' | 'Succeeded' (ReadOnly)
* **secondaryEndpoints**: Endpoints (ReadOnly)
* **secondaryLocation**: string (ReadOnly)
* **statusOfPrimary**: 'Available' | 'Unavailable' (ReadOnly)
* **statusOfSecondary**: 'Available' | 'Unavailable' (ReadOnly)

## CustomDomain
### Properties
* **name**: string (ReadOnly)
* **useSubDomainName**: bool (ReadOnly)

## Endpoints
### Properties
* **blob**: string (ReadOnly)
* **queue**: string (ReadOnly)
* **table**: string (ReadOnly)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

