# Microsoft.Capacity @ 2019-07-19-preview

## Resource Microsoft.Capacity/resourceProviders/locations/serviceLimits@2019-07-19-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2019-07-19-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: QuotaProperties
* **type**: 'Microsoft.Capacity/resourceProviders/locations/serviceLimits' (ReadOnly, DeployTimeConstant)

## QuotaProperties
### Properties
* **currentValue**: int (ReadOnly)
* **limit**: int
* **name**: ResourceName
* **properties**: any
* **quotaPeriod**: string (ReadOnly)
* **resourceType**: any
* **unit**: string

## ResourceName
### Properties
* **localizedValue**: string (ReadOnly)
* **value**: string

