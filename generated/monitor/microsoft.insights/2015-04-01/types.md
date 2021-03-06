# microsoft.insights @ 2015-04-01

## Resource microsoft.insights/autoscalesettings@2015-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-04-01' (ReadOnly, DeployTimeConstant)
* **dependsOn**: resourceref[] (WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: AutoscaleSetting (Required)
* **tags**: Dictionary<string,String>
* **type**: 'microsoft.insights/autoscalesettings' (ReadOnly, DeployTimeConstant)

## AutoscaleSetting
### Properties
* **enabled**: bool
* **name**: string
* **notifications**: AutoscaleNotification[]
* **profiles**: AutoscaleProfile[] (Required)
* **targetResourceUri**: string

## AutoscaleNotification
### Properties
* **email**: EmailNotification
* **operation**: string (Required)
* **webhooks**: WebhookNotification[]

## EmailNotification
### Properties
* **customEmails**: string[]
* **sendToSubscriptionAdministrator**: bool
* **sendToSubscriptionCoAdministrators**: bool

## WebhookNotification
### Properties
* **properties**: Dictionary<string,String>
* **serviceUri**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## AutoscaleProfile
### Properties
* **capacity**: ScaleCapacity (Required)
* **fixedDate**: TimeWindow
* **name**: string (Required)
* **recurrence**: Recurrence
* **rules**: ScaleRule[] (Required)

## ScaleCapacity
### Properties
* **default**: string (Required)
* **maximum**: string (Required)
* **minimum**: string (Required)

## TimeWindow
### Properties
* **end**: string (Required)
* **start**: string (Required)
* **timeZone**: string

## Recurrence
### Properties
* **frequency**: 'Day' | 'Hour' | 'Minute' | 'Month' | 'None' | 'Second' | 'Week' | 'Year' (Required)
* **schedule**: RecurrentSchedule (Required)

## RecurrentSchedule
### Properties
* **days**: string[] (Required)
* **hours**: int[] (Required)
* **minutes**: int[] (Required)
* **timeZone**: string (Required)

## ScaleRule
### Properties
* **metricTrigger**: MetricTrigger (Required)
* **scaleAction**: ScaleAction (Required)

## MetricTrigger
### Properties
* **dimensions**: ScaleRuleMetricDimension[]
* **metricName**: string (Required)
* **metricNamespace**: string
* **metricResourceUri**: string (Required)
* **operator**: 'Equals' | 'GreaterThan' | 'GreaterThanOrEqual' | 'LessThan' | 'LessThanOrEqual' | 'NotEquals' (Required)
* **statistic**: 'Average' | 'Max' | 'Min' | 'Sum' (Required)
* **threshold**: int (Required)
* **timeAggregation**: 'Average' | 'Count' | 'Last' | 'Maximum' | 'Minimum' | 'Total' (Required)
* **timeGrain**: string (Required)
* **timeWindow**: string (Required)

## ScaleRuleMetricDimension
### Properties
* **DimensionName**: string (Required)
* **Operator**: 'Equals' | 'NotEquals' (Required)
* **Values**: string[] (Required)

## ScaleAction
### Properties
* **cooldown**: string (Required)
* **direction**: 'Decrease' | 'Increase' | 'None' (Required)
* **type**: 'ChangeCount' | 'ExactCount' | 'PercentChangeCount' (Required)
* **value**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

