# Microsoft.Subscription @ 2020-09-01

## Microsoft.Subscription/aliases
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: PutAliasRequestProperties (Required)
* **type**: 'Microsoft.Subscription/aliases' (ReadOnly, DeployTimeConstant)

## PutAliasRequestProperties
### Properties
* **billingScope**: string (WriteOnly)
* **displayName**: string (WriteOnly)
* **provisioningState**: 'Accepted' | 'Failed' | 'Succeeded' (ReadOnly)
* **resellerId**: string (WriteOnly)
* **subscriptionId**: string
* **workload**: 'DevTest' | 'Production' (WriteOnly)
