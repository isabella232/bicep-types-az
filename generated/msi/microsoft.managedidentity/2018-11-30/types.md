# Microsoft.ManagedIdentity @ 2018-11-30

## Resource Microsoft.ManagedIdentity/userAssignedIdentities@2018-11-30
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-11-30' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: UserAssignedIdentityProperties (ReadOnly)
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.ManagedIdentity/userAssignedIdentities' (ReadOnly, DeployTimeConstant)

## UserAssignedIdentityProperties
### Properties
* **clientId**: string (ReadOnly)
* **principalId**: string (ReadOnly)
* **tenantId**: string (ReadOnly)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

