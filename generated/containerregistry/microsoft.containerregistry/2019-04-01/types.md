# Microsoft.ContainerRegistry @ 2019-04-01

## Resource Microsoft.ContainerRegistry/registries/tasks@2019-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-04-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **identity**: IdentityProperties
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: TaskProperties
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.ContainerRegistry/registries/tasks' (ReadOnly, DeployTimeConstant)

## IdentityProperties
### Properties
* **principalId**: string
* **tenantId**: string
* **type**: 'None' | 'SystemAssigned, UserAssigned' | 'SystemAssigned' | 'UserAssigned'
* **userAssignedIdentities**: Dictionary<string,UserIdentityProperties>

## Dictionary<string,UserIdentityProperties>
### Properties
### Additional Properties
* **Additional Properties Type**: UserIdentityProperties

## UserIdentityProperties
### Properties
* **clientId**: string
* **principalId**: string

## TaskProperties
### Properties
* **agentConfiguration**: AgentProperties
* **creationDate**: string (ReadOnly)
* **credentials**: Credentials
* **platform**: PlatformProperties (Required)
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly)
* **status**: 'Disabled' | 'Enabled'
* **step**: TaskStepProperties (Required)
* **timeout**: int
* **trigger**: TriggerProperties

## AgentProperties
### Properties
* **cpu**: int

## Credentials
### Properties
* **customRegistries**: Dictionary<string,CustomRegistryCredentials>
* **sourceRegistry**: SourceRegistryCredentials

## Dictionary<string,CustomRegistryCredentials>
### Properties
### Additional Properties
* **Additional Properties Type**: CustomRegistryCredentials

## CustomRegistryCredentials
### Properties
* **identity**: string
* **password**: SecretObject
* **userName**: SecretObject

## SecretObject
### Properties
* **type**: 'Opaque' | 'Vaultsecret'
* **value**: string

## SourceRegistryCredentials
### Properties
* **loginMode**: 'Default' | 'None'

## PlatformProperties
### Properties
* **architecture**: 'amd64' | 'arm' | 'x86'
* **os**: 'Linux' | 'Windows' (Required)
* **variant**: 'v6' | 'v7' | 'v8'

## TaskStepProperties
* **Discriminator**: type
### Base Properties
* **baseImageDependencies**: BaseImageDependency[] (ReadOnly)
* **contextAccessToken**: string
* **contextPath**: string
### Docker
#### Properties
* **arguments**: Argument[]
* **dockerFilePath**: string (Required)
* **imageNames**: string[]
* **isPushEnabled**: bool
* **noCache**: bool
* **target**: string
* **type**: 'Docker' (Required)

### EncodedTask
#### Properties
* **encodedTaskContent**: string (Required)
* **encodedValuesContent**: string
* **type**: 'EncodedTask' (Required)
* **values**: SetValue[]

### FileTask
#### Properties
* **taskFilePath**: string (Required)
* **type**: 'FileTask' (Required)
* **values**: SetValue[]
* **valuesFilePath**: string


## BaseImageDependency
### Properties
* **digest**: string
* **registry**: string
* **repository**: string
* **tag**: string
* **type**: 'BuildTime' | 'RunTime'

## Docker
### Properties
* **arguments**: Argument[]
* **dockerFilePath**: string (Required)
* **imageNames**: string[]
* **isPushEnabled**: bool
* **noCache**: bool
* **target**: string
* **type**: 'Docker' (Required)

## Argument
### Properties
* **isSecret**: bool
* **name**: string (Required)
* **value**: string (Required)

## EncodedTask
### Properties
* **encodedTaskContent**: string (Required)
* **encodedValuesContent**: string
* **type**: 'EncodedTask' (Required)
* **values**: SetValue[]

## SetValue
### Properties
* **isSecret**: bool
* **name**: string (Required)
* **value**: string (Required)

## FileTask
### Properties
* **taskFilePath**: string (Required)
* **type**: 'FileTask' (Required)
* **values**: SetValue[]
* **valuesFilePath**: string

## TriggerProperties
### Properties
* **baseImageTrigger**: BaseImageTrigger
* **sourceTriggers**: SourceTrigger[]
* **timerTriggers**: TimerTrigger[]

## BaseImageTrigger
### Properties
* **baseImageTriggerType**: 'All' | 'Runtime' (Required)
* **name**: string (Required)
* **status**: 'Disabled' | 'Enabled'

## SourceTrigger
### Properties
* **name**: string (Required)
* **sourceRepository**: SourceProperties (Required)
* **sourceTriggerEvents**: 'commit' | 'pullrequest'[] (Required)
* **status**: 'Disabled' | 'Enabled'

## SourceProperties
### Properties
* **branch**: string
* **repositoryUrl**: string (Required)
* **sourceControlAuthProperties**: AuthInfo
* **sourceControlType**: 'Github' | 'VisualStudioTeamService' (Required)

## AuthInfo
### Properties
* **expiresIn**: int
* **refreshToken**: string
* **scope**: string
* **token**: string (Required)
* **tokenType**: 'OAuth' | 'PAT' (Required)

## TimerTrigger
### Properties
* **name**: string (Required)
* **schedule**: string (Required)
* **status**: 'Disabled' | 'Enabled'

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

