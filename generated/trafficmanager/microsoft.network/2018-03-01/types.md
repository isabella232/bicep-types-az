# Microsoft.Network @ 2018-03-01

## Resource Microsoft.Network/trafficmanagerprofiles@2018-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-03-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string
* **name**: string (Required, DeployTimeConstant)
* **properties**: ProfileProperties
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.Network/trafficmanagerprofiles' (ReadOnly, DeployTimeConstant)

## ProfileProperties
### Properties
* **dnsConfig**: DnsConfig
* **endpoints**: Endpoint[]
* **monitorConfig**: MonitorConfig
* **profileStatus**: 'Disabled' | 'Enabled'
* **trafficRoutingMethod**: 'Geographic' | 'Performance' | 'Priority' | 'Weighted'
* **trafficViewEnrollmentStatus**: 'Disabled' | 'Enabled'

## DnsConfig
### Properties
* **fqdn**: string (ReadOnly)
* **relativeName**: string
* **ttl**: int

## Endpoint
### Properties
* **id**: string
* **name**: string
* **properties**: EndpointProperties
* **type**: string

## EndpointProperties
### Properties
* **customHeaders**: schemas:1_customHeadersItem[]
* **endpointLocation**: string
* **endpointMonitorStatus**: 'CheckingEndpoint' | 'Degraded' | 'Disabled' | 'Inactive' | 'Online' | 'Stopped'
* **endpointStatus**: 'Disabled' | 'Enabled'
* **geoMapping**: string[]
* **minChildEndpoints**: int
* **priority**: int
* **target**: string
* **targetResourceId**: string
* **weight**: int

## schemas:1_customHeadersItem
### Properties
* **name**: string
* **value**: string

## MonitorConfig
### Properties
* **customHeaders**: schemas:1_customHeadersItem[]
* **expectedStatusCodeRanges**: schemas:10_expectedStatusCodeRangesItem[]
* **intervalInSeconds**: int
* **path**: string
* **port**: int
* **profileMonitorStatus**: 'CheckingEndpoints' | 'Degraded' | 'Disabled' | 'Inactive' | 'Online'
* **protocol**: 'HTTP' | 'HTTPS' | 'TCP'
* **timeoutInSeconds**: int
* **toleratedNumberOfFailures**: int

## schemas:10_expectedStatusCodeRangesItem
### Properties
* **max**: int
* **min**: int

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

