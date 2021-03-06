# Microsoft.Compute.Admin @ 2015-12-01-preview

## Resource Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions@2015-12-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2015-12-01-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (ReadOnly)
* **name**: string (Required, DeployTimeConstant)
* **properties**: PlatformImageProperties
* **type**: 'Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions@2015-12-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2015-12-01-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (ReadOnly)
* **name**: string (Required, DeployTimeConstant)
* **properties**: VMExtensionProperties
* **type**: 'Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions' (ReadOnly, DeployTimeConstant)

## PlatformImageProperties
### Properties
* **dataDisks**: DataDisk[]
* **details**: ImageDetails
* **osDisk**: OsDisk
* **provisioningState**: 'Canceled' | 'Creating' | 'Failed' | 'Succeeded'

## DataDisk
### Properties
* **lun**: int
* **uri**: string

## ImageDetails
### Properties
* **billingPartNumber**: string

## OsDisk
### Properties
* **osType**: 'Linux' | 'Unknown' | 'Windows'
* **uri**: string

## VMExtensionProperties
### Properties
* **computeRole**: string
* **isSystemExtension**: bool
* **provisioningState**: 'Canceled' | 'Creating' | 'Failed' | 'Succeeded'
* **publisher**: string
* **sourceBlob**: AzureBlob
* **supportMultipleExtensions**: bool
* **vmOsType**: 'Linux' | 'Unknown' | 'Windows'
* **vmScaleSetEnabled**: bool

## AzureBlob
### Properties
* **uri**: string

