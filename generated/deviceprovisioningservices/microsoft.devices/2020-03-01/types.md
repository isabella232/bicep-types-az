# Microsoft.Devices @ 2020-03-01

## Resource Microsoft.Devices/provisioningServices@2020-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-03-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: IotDpsPropertiesDescription (Required)
* **sku**: IotDpsSkuInfo (Required)
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.Devices/provisioningServices' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Devices/provisioningServices/certificates@2020-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-03-01' (ReadOnly, DeployTimeConstant)
* **certificate**: string (WriteOnly)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: CertificateProperties (ReadOnly)
* **type**: 'Microsoft.Devices/provisioningServices/certificates' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Devices/provisioningServices/privateEndpointConnections@2020-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-03-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: PrivateEndpointConnectionProperties (Required)
* **type**: 'Microsoft.Devices/provisioningServices/privateEndpointConnections' (ReadOnly, DeployTimeConstant)

## IotDpsPropertiesDescription
### Properties
* **allocationPolicy**: 'GeoLatency' | 'Hashed' | 'Static'
* **authorizationPolicies**: SharedAccessSignatureAuthorizationRule_AccessRightsDescription_[]
* **deviceProvisioningHostName**: string (ReadOnly)
* **idScope**: string (ReadOnly)
* **iotHubs**: IotHubDefinitionDescription[]
* **ipFilterRules**: IpFilterRule[]
* **privateEndpointConnections**: PrivateEndpointConnection[]
* **provisioningState**: string
* **publicNetworkAccess**: 'Disabled' | 'Enabled'
* **serviceOperationsHostName**: string (ReadOnly)
* **state**: 'Activating' | 'ActivationFailed' | 'Active' | 'Deleted' | 'Deleting' | 'DeletionFailed' | 'FailingOver' | 'FailoverFailed' | 'Resuming' | 'Suspended' | 'Suspending' | 'Transitioning'

## SharedAccessSignatureAuthorizationRule_AccessRightsDescription_
### Properties
* **keyName**: string (Required)
* **primaryKey**: string
* **rights**: 'DeviceConnect' | 'EnrollmentRead' | 'EnrollmentWrite' | 'RegistrationStatusRead' | 'RegistrationStatusWrite' | 'ServiceConfig' (Required)
* **secondaryKey**: string

## IotHubDefinitionDescription
### Properties
* **allocationWeight**: int
* **applyAllocationPolicy**: bool
* **connectionString**: string (Required)
* **location**: string (Required)
* **name**: string (ReadOnly)

## IpFilterRule
### Properties
* **action**: 'Accept' | 'Reject' (Required)
* **filterName**: string (Required)
* **ipMask**: string (Required)
* **target**: 'all' | 'deviceApi' | 'serviceApi'

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly)
* **name**: string (ReadOnly)
* **properties**: PrivateEndpointConnectionProperties (Required)
* **type**: string (ReadOnly)

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: PrivateEndpoint
* **privateLinkServiceConnectionState**: PrivateLinkServiceConnectionState (Required)

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly)

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string
* **description**: string (Required)
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' (Required)

## IotDpsSkuInfo
### Properties
* **capacity**: int
* **name**: 'S1'
* **tier**: string (ReadOnly)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## CertificateProperties
### Properties
* **created**: string (ReadOnly)
* **expiry**: string (ReadOnly)
* **isVerified**: bool (ReadOnly)
* **subject**: string (ReadOnly)
* **thumbprint**: string (ReadOnly)
* **updated**: string (ReadOnly)

