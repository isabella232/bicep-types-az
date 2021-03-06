# Microsoft.Security @ 2020-01-01-preview

## Resource Microsoft.Security/connectors@2020-01-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-01-01-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: ConnectorSettingProperties
* **type**: 'Microsoft.Security/connectors' (ReadOnly, DeployTimeConstant)

## ConnectorSettingProperties
### Properties
* **authenticationDetails**: AuthenticationDetailsProperties
* **hybridComputeSettings**: HybridComputeSettingsProperties

## AuthenticationDetailsProperties
* **Discriminator**: authenticationType
### Base Properties
* **authenticationProvisioningState**: 'Expired' | 'IncorrectPolicy' | 'Invalid' | 'Valid' (ReadOnly)
* **grantedPermissions**: 'AWS::AmazonSSMAutomationRole' | 'AWS::AWSSecurityHubReadOnlyAccess' | 'AWS::SecurityAudit' | 'GCP::Security Center Admin Viewer'[] (ReadOnly)
### awsAssumeRole
#### Properties
* **accountId**: string (ReadOnly)
* **authenticationType**: 'awsAssumeRole' (Required)
* **awsAssumeRoleArn**: string (Required)
* **awsExternalId**: string (Required)

### awsCreds
#### Properties
* **accountId**: string (ReadOnly)
* **authenticationType**: 'awsCreds' (Required)
* **awsAccessKeyId**: string (Required)
* **awsSecretAccessKey**: string (Required)

### gcpCredentials
#### Properties
* **authenticationType**: 'gcpCredentials' (Required)
* **authProviderX509CertUrl**: string (Required)
* **authUri**: string (Required)
* **clientEmail**: string (Required)
* **clientId**: string (Required)
* **clientX509CertUrl**: string (Required)
* **organizationId**: string (Required)
* **privateKey**: string (Required)
* **privateKeyId**: string (Required)
* **projectId**: string (Required)
* **tokenUri**: string (Required)
* **type**: string (Required)


## awsAssumeRole
### Properties
* **accountId**: string (ReadOnly)
* **authenticationType**: 'awsAssumeRole' (Required)
* **awsAssumeRoleArn**: string (Required)
* **awsExternalId**: string (Required)

## awsCreds
### Properties
* **accountId**: string (ReadOnly)
* **authenticationType**: 'awsCreds' (Required)
* **awsAccessKeyId**: string (Required)
* **awsSecretAccessKey**: string (Required)

## gcpCredentials
### Properties
* **authenticationType**: 'gcpCredentials' (Required)
* **authProviderX509CertUrl**: string (Required)
* **authUri**: string (Required)
* **clientEmail**: string (Required)
* **clientId**: string (Required)
* **clientX509CertUrl**: string (Required)
* **organizationId**: string (Required)
* **privateKey**: string (Required)
* **privateKeyId**: string (Required)
* **projectId**: string (Required)
* **tokenUri**: string (Required)
* **type**: string (Required)

## HybridComputeSettingsProperties
### Properties
* **autoProvision**: 'Off' | 'On' (Required)
* **hybridComputeProvisioningState**: 'Expired' | 'Invalid' | 'Valid' (ReadOnly)
* **proxyServer**: ProxyServerProperties
* **region**: string
* **resourceGroupName**: string
* **servicePrincipal**: ServicePrincipalProperties

## ProxyServerProperties
### Properties
* **ip**: string
* **port**: string

## ServicePrincipalProperties
### Properties
* **applicationId**: string
* **secret**: string

