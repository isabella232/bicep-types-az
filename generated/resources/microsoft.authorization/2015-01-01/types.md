# Microsoft.Authorization @ 2015-01-01

## Resource Microsoft.Authorization/locks@2015-01-01
* **Valid Scope(s)**: Subscription, ResourceGroup, Extension
### Properties
* **apiVersion**: '2015-01-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: ManagementLockProperties
* **type**: 'Microsoft.Authorization/locks' (ReadOnly, DeployTimeConstant)

## ManagementLockProperties
### Properties
* **level**: 'CanNotDelete' | 'NotSpecified' | 'ReadOnly'
* **notes**: string

