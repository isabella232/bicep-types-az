# Microsoft.Batch @ 2020-09-01

## Resource Microsoft.Batch/batchAccounts@2020-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **identity**: BatchAccountIdentity
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: BatchAccountCreateProperties
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.Batch/batchAccounts' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Batch/batchAccounts/applications@2020-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: ApplicationProperties
* **type**: 'Microsoft.Batch/batchAccounts/applications' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Batch/batchAccounts/applications/versions@2020-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: ApplicationPackageProperties
* **type**: 'Microsoft.Batch/batchAccounts/applications/versions' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Batch/batchAccounts/certificates@2020-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: CertificateCreateOrUpdateProperties
* **type**: 'Microsoft.Batch/batchAccounts/certificates' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Batch/batchAccounts/pools@2020-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-09-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: PoolProperties
* **type**: 'Microsoft.Batch/batchAccounts/pools' (ReadOnly, DeployTimeConstant)

## BatchAccountIdentity
### Properties
* **principalId**: string (ReadOnly)
* **tenantId**: string (ReadOnly)
* **type**: 'None' | 'SystemAssigned' (Required)

## BatchAccountCreateProperties
### Properties
* **accountEndpoint**: string (ReadOnly)
* **activeJobAndJobScheduleQuota**: int (ReadOnly)
* **autoStorage**: AutoStorageBaseProperties
* **dedicatedCoreQuota**: int (ReadOnly)
* **dedicatedCoreQuotaPerVMFamily**: VirtualMachineFamilyCoreQuota[] (ReadOnly)
* **dedicatedCoreQuotaPerVMFamilyEnforced**: bool (ReadOnly)
* **encryption**: EncryptionProperties
* **keyVaultReference**: KeyVaultReference
* **lowPriorityCoreQuota**: int (ReadOnly)
* **poolAllocationMode**: 'BatchService' | 'UserSubscription'
* **poolQuota**: int (ReadOnly)
* **privateEndpointConnections**: PrivateEndpointConnection[] (ReadOnly)
* **provisioningState**: 'Cancelled' | 'Creating' | 'Deleting' | 'Failed' | 'Invalid' | 'Succeeded' (ReadOnly)
* **publicNetworkAccess**: 'Disabled' | 'Enabled'

## AutoStorageBaseProperties
### Properties
* **lastKeySync**: string (ReadOnly)
* **storageAccountId**: string (Required)

## VirtualMachineFamilyCoreQuota
### Properties
* **coreQuota**: int (ReadOnly)
* **name**: string (ReadOnly)

## EncryptionProperties
### Properties
* **keySource**: 'Microsoft.Batch' | 'Microsoft.KeyVault'
* **keyVaultProperties**: KeyVaultProperties

## KeyVaultProperties
### Properties
* **keyIdentifier**: string

## KeyVaultReference
### Properties
* **id**: string (Required)
* **url**: string (Required)

## PrivateEndpointConnection
### Properties
* **etag**: string (ReadOnly)
* **id**: string (ReadOnly)
* **name**: string (ReadOnly)
* **properties**: PrivateEndpointConnectionProperties (ReadOnly)
* **type**: string (ReadOnly)

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: PrivateEndpoint (ReadOnly)
* **privateLinkServiceConnectionState**: PrivateLinkServiceConnectionState (ReadOnly)
* **provisioningState**: 'Failed' | 'Succeeded' | 'Updating' (ReadOnly)

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly)

## PrivateLinkServiceConnectionState
### Properties
* **actionRequired**: string (ReadOnly)
* **description**: string (ReadOnly)
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' (ReadOnly)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ApplicationProperties
### Properties
* **allowUpdates**: bool
* **defaultVersion**: string
* **displayName**: string

## ApplicationPackageProperties
### Properties
* **format**: string (ReadOnly)
* **lastActivationTime**: string (ReadOnly)
* **state**: 'Active' | 'Pending' (ReadOnly)
* **storageUrl**: string (ReadOnly)
* **storageUrlExpiry**: string (ReadOnly)

## CertificateCreateOrUpdateProperties
### Properties
* **data**: string (Required, WriteOnly)
* **deleteCertificateError**: DeleteCertificateError (ReadOnly)
* **format**: 'Cer' | 'Pfx'
* **password**: string (WriteOnly)
* **previousProvisioningState**: 'Deleting' | 'Failed' | 'Succeeded' (ReadOnly)
* **previousProvisioningStateTransitionTime**: string (ReadOnly)
* **provisioningState**: 'Deleting' | 'Failed' | 'Succeeded' (ReadOnly)
* **provisioningStateTransitionTime**: string (ReadOnly)
* **publicData**: string (ReadOnly)
* **thumbprint**: string
* **thumbprintAlgorithm**: string

## DeleteCertificateError
### Properties
* **code**: string (ReadOnly)
* **details**: DeleteCertificateError[] (ReadOnly)
* **message**: string (ReadOnly)
* **target**: string (ReadOnly)

## PoolProperties
### Properties
* **allocationState**: 'Resizing' | 'Steady' | 'Stopping' (ReadOnly)
* **allocationStateTransitionTime**: string (ReadOnly)
* **applicationLicenses**: string[]
* **applicationPackages**: ApplicationPackageReference[]
* **autoScaleRun**: AutoScaleRun (ReadOnly)
* **certificates**: CertificateReference[]
* **creationTime**: string (ReadOnly)
* **currentDedicatedNodes**: int (ReadOnly)
* **currentLowPriorityNodes**: int (ReadOnly)
* **deploymentConfiguration**: DeploymentConfiguration
* **displayName**: string
* **interNodeCommunication**: 'Disabled' | 'Enabled'
* **lastModified**: string (ReadOnly)
* **metadata**: MetadataItem[]
* **mountConfiguration**: MountConfiguration[]
* **networkConfiguration**: NetworkConfiguration
* **provisioningState**: 'Deleting' | 'Succeeded' (ReadOnly)
* **provisioningStateTransitionTime**: string (ReadOnly)
* **resizeOperationStatus**: ResizeOperationStatus (ReadOnly)
* **scaleSettings**: ScaleSettings
* **startTask**: StartTask
* **taskSchedulingPolicy**: TaskSchedulingPolicy
* **taskSlotsPerNode**: int
* **userAccounts**: UserAccount[]
* **vmSize**: string

## ApplicationPackageReference
### Properties
* **id**: string (Required)
* **version**: string

## AutoScaleRun
### Properties
* **error**: AutoScaleRunError
* **evaluationTime**: string (Required)
* **results**: string

## AutoScaleRunError
### Properties
* **code**: string (Required)
* **details**: AutoScaleRunError[]
* **message**: string (Required)

## CertificateReference
### Properties
* **id**: string (Required)
* **storeLocation**: 'CurrentUser' | 'LocalMachine'
* **storeName**: string
* **visibility**: 'RemoteUser' | 'StartTask' | 'Task'[]

## DeploymentConfiguration
### Properties
* **cloudServiceConfiguration**: CloudServiceConfiguration
* **virtualMachineConfiguration**: VirtualMachineConfiguration

## CloudServiceConfiguration
### Properties
* **osFamily**: string (Required)
* **osVersion**: string

## VirtualMachineConfiguration
### Properties
* **containerConfiguration**: ContainerConfiguration
* **dataDisks**: DataDisk[]
* **diskEncryptionConfiguration**: DiskEncryptionConfiguration
* **imageReference**: ImageReference (Required)
* **licenseType**: string
* **nodeAgentSkuId**: string (Required)
* **windowsConfiguration**: WindowsConfiguration

## ContainerConfiguration
### Properties
* **containerImageNames**: string[]
* **containerRegistries**: ContainerRegistry[]
* **type**: string (Required)

## ContainerRegistry
### Properties
* **password**: string (Required)
* **registryServer**: string
* **username**: string (Required)

## DataDisk
### Properties
* **caching**: 'None' | 'ReadOnly' | 'ReadWrite'
* **diskSizeGB**: int (Required)
* **lun**: int (Required)
* **storageAccountType**: 'Premium_LRS' | 'Standard_LRS'

## DiskEncryptionConfiguration
### Properties
* **targets**: 'OsDisk' | 'TemporaryDisk'[]

## ImageReference
### Properties
* **id**: string
* **offer**: string
* **publisher**: string
* **sku**: string
* **version**: string

## WindowsConfiguration
### Properties
* **enableAutomaticUpdates**: bool

## MetadataItem
### Properties
* **name**: string (Required)
* **value**: string (Required)

## MountConfiguration
### Properties
* **azureBlobFileSystemConfiguration**: AzureBlobFileSystemConfiguration
* **azureFileShareConfiguration**: AzureFileShareConfiguration
* **cifsMountConfiguration**: CIFSMountConfiguration
* **nfsMountConfiguration**: NFSMountConfiguration

## AzureBlobFileSystemConfiguration
### Properties
* **accountKey**: string
* **accountName**: string (Required)
* **blobfuseOptions**: string
* **containerName**: string (Required)
* **relativeMountPath**: string (Required)
* **sasKey**: string

## AzureFileShareConfiguration
### Properties
* **accountKey**: string (Required)
* **accountName**: string (Required)
* **azureFileUrl**: string (Required)
* **mountOptions**: string
* **relativeMountPath**: string (Required)

## CIFSMountConfiguration
### Properties
* **mountOptions**: string
* **password**: string (Required)
* **relativeMountPath**: string (Required)
* **source**: string (Required)
* **username**: string (Required)

## NFSMountConfiguration
### Properties
* **mountOptions**: string
* **relativeMountPath**: string (Required)
* **source**: string (Required)

## NetworkConfiguration
### Properties
* **endpointConfiguration**: PoolEndpointConfiguration
* **publicIPAddressConfiguration**: PublicIPAddressConfiguration
* **subnetId**: string

## PoolEndpointConfiguration
### Properties
* **inboundNatPools**: InboundNatPool[] (Required)

## InboundNatPool
### Properties
* **backendPort**: int (Required)
* **frontendPortRangeEnd**: int (Required)
* **frontendPortRangeStart**: int (Required)
* **name**: string (Required)
* **networkSecurityGroupRules**: NetworkSecurityGroupRule[]
* **protocol**: 'TCP' | 'UDP' (Required)

## NetworkSecurityGroupRule
### Properties
* **access**: 'Allow' | 'Deny' (Required)
* **priority**: int (Required)
* **sourceAddressPrefix**: string (Required)
* **sourcePortRanges**: string[]

## PublicIPAddressConfiguration
### Properties
* **ipAddressIds**: string[]
* **provision**: 'BatchManaged' | 'NoPublicIPAddresses' | 'UserManaged'

## ResizeOperationStatus
### Properties
* **errors**: ResizeError[]
* **nodeDeallocationOption**: 'Requeue' | 'RetainedData' | 'TaskCompletion' | 'Terminate'
* **resizeTimeout**: string
* **startTime**: string
* **targetDedicatedNodes**: int
* **targetLowPriorityNodes**: int

## ResizeError
### Properties
* **code**: string (Required)
* **details**: ResizeError[]
* **message**: string (Required)

## ScaleSettings
### Properties
* **autoScale**: AutoScaleSettings
* **fixedScale**: FixedScaleSettings

## AutoScaleSettings
### Properties
* **evaluationInterval**: string
* **formula**: string (Required)

## FixedScaleSettings
### Properties
* **nodeDeallocationOption**: 'Requeue' | 'RetainedData' | 'TaskCompletion' | 'Terminate'
* **resizeTimeout**: string
* **targetDedicatedNodes**: int
* **targetLowPriorityNodes**: int

## StartTask
### Properties
* **commandLine**: string
* **containerSettings**: TaskContainerSettings
* **environmentSettings**: EnvironmentSetting[]
* **maxTaskRetryCount**: int
* **resourceFiles**: ResourceFile[]
* **userIdentity**: UserIdentity
* **waitForSuccess**: bool

## TaskContainerSettings
### Properties
* **containerRunOptions**: string
* **imageName**: string (Required)
* **registry**: ContainerRegistry
* **workingDirectory**: 'ContainerImageDefault' | 'TaskWorkingDirectory'

## EnvironmentSetting
### Properties
* **name**: string (Required)
* **value**: string

## ResourceFile
### Properties
* **autoStorageContainerName**: string
* **blobPrefix**: string
* **fileMode**: string
* **filePath**: string
* **httpUrl**: string
* **storageContainerUrl**: string

## UserIdentity
### Properties
* **autoUser**: AutoUserSpecification
* **userName**: string

## AutoUserSpecification
### Properties
* **elevationLevel**: 'Admin' | 'NonAdmin'
* **scope**: 'Pool' | 'Task'

## TaskSchedulingPolicy
### Properties
* **nodeFillType**: 'Pack' | 'Spread' (Required)

## UserAccount
### Properties
* **elevationLevel**: 'Admin' | 'NonAdmin'
* **linuxUserConfiguration**: LinuxUserConfiguration
* **name**: string (Required)
* **password**: string (Required)
* **windowsUserConfiguration**: WindowsUserConfiguration

## LinuxUserConfiguration
### Properties
* **gid**: int
* **sshPrivateKey**: string
* **uid**: int

## WindowsUserConfiguration
### Properties
* **loginMode**: 'Batch' | 'Interactive'

