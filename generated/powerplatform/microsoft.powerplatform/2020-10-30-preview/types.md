# Microsoft.PowerPlatform @ 2020-10-30-preview

## Resource Microsoft.PowerPlatform/enterprisePolicies@2020-10-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-30-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **identity**: EnterprisePolicyIdentity
* **location**: string (ReadOnly)
* **name**: string (Required, DeployTimeConstant)
* **properties**: Properties
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.PowerPlatform/enterprisePolicies' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.PowerPlatform/enterprisePolicies/privateEndpointConnections@2020-10-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-30-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (ReadOnly)
* **name**: string (Required, DeployTimeConstant)
* **properties**: PrivateEndpointConnectionProperties
* **type**: 'Microsoft.PowerPlatform/enterprisePolicies/privateEndpointConnections' (ReadOnly, DeployTimeConstant)

## EnterprisePolicyIdentity
### Properties
* **systemAssignedIdentityPrincipalId**: string (ReadOnly)
* **tenantId**: string (ReadOnly)
* **type**: 'None' | 'SystemAssigned'

## Properties
### Properties
* **encryption**: schemas:1_encryption
* **lockbox**: schemas:1_lockbox
* **systemData**: systemData

## schemas:1_encryption
### Properties
* **keyVaultProperties**: KeyVaultProperties

## KeyVaultProperties
### Properties
* **id**: string
* **key**: keyProperties
* **status**: 'Disabled' | 'Enabled' | 'NotConfigured'

## keyProperties
### Properties
* **name**: string
* **version**: string

## schemas:1_lockbox
### Properties
* **status**: 'Disabled' | 'Enabled' | 'NotConfigured'

## systemData
### Properties
* **createdAt**: string
* **createdBy**: string
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User'
* **lastModifiedAt**: string
* **lastModifiedBy**: string
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User'

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: PrivateEndpoint
* **privateLinkServiceConnectionState**: PrivateLinkServiceConnectionState (Required)
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded'

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly)

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string
* **description**: string
* **status**: 'Approved' | 'Pending' | 'Rejected'

