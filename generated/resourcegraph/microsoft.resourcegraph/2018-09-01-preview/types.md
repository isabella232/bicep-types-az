# Microsoft.ResourceGraph @ 2018-09-01-preview

## Resource Microsoft.ResourceGraph/queries@2018-09-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-09-01-preview' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **eTag**: string
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string
* **name**: string (Required, DeployTimeConstant)
* **properties**: GraphQueryProperties
* **tags**: Dictionary<string,String>
* **type**: 'Microsoft.ResourceGraph/queries' (ReadOnly, DeployTimeConstant)

## GraphQueryProperties
### Properties
* **description**: string
* **query**: string (Required)
* **resultKind**: 'basic' (ReadOnly)
* **timeModified**: string (ReadOnly)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

