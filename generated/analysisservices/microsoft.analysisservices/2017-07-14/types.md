# Microsoft.AnalysisServices @ 2017-07-14

## Resource Microsoft.AnalysisServices/servers@2017-07-14
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2017-07-14' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: AnalysisServicesServerProperties
* **sku**: ResourceSku (Required)
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.AnalysisServices/servers' (ReadOnly, DeployTimeConstant)

## AnalysisServicesServerProperties
### Properties
* **asAdministrators**: ServerAdministrators
* **backupBlobContainerUri**: string
* **gatewayDetails**: GatewayDetails
* **provisioningState**: 'Deleting' | 'Failed' | 'Paused' | 'Pausing' | 'Preparing' | 'Provisioning' | 'Resuming' | 'Scaling' | 'Succeeded' | 'Suspended' | 'Suspending' | 'Updating' (ReadOnly)
* **serverFullName**: string (ReadOnly)
* **state**: 'Deleting' | 'Failed' | 'Paused' | 'Pausing' | 'Preparing' | 'Provisioning' | 'Resuming' | 'Scaling' | 'Succeeded' | 'Suspended' | 'Suspending' | 'Updating' (ReadOnly)

## ServerAdministrators
### Properties
* **members**: string[]

## GatewayDetails
### Properties
* **dmtsClusterUri**: string (ReadOnly)
* **gatewayObjectId**: string (ReadOnly)
* **gatewayResourceId**: string

## ResourceSku
### Properties
* **name**: string (Required)
* **tier**: 'Basic' | 'Development' | 'Standard'

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

