# Marain.Deployment

This repository is used to help manage the deployments of your own [Marain](https://github.com/marain-dotnet/) instances.

By default the pipeline models three environments:
- marain_dev
- marain_test
- marain_prod

>NOTE: Whilst Azure DevOps will automatically create the environments you will need to add manual approvals to, at least, all but the 'dev' environment.

## Getting Started

### Global Variables
These variables are values that are intended to be the same across all environments - initially they are defined the following default values:

|Name | Default | Description
|-----|---------|------------
|Marain_InstanceType | Stable | sets which release channel to use (valid options: Stable or Development)
|Marain_ResourcePrefix | mar | the naming-convention prefix for all resources. If necessary, this can be overridden for a particular environment.




### Environment-specific Variables
Each environment requires the following variables to be set - initially they are defined with the following placeholder values:

|Name | Default | Description
|-----|---------|------------
Marain_AzureLocation|<REPLACE_ME>| The Azure location for the deployment
Marain_AzureSubscriptionId|<REPLACE_ME>| The subscription ID into which Marain should be deployed
Marain_AzureTenantId|<REPLACE_ME>| The Azure tenant ID for the above subscription
Marain_ServiceConnectionName|<REPLACE_ME>| The name of the Azure DevOps AzureRM service connection with permissions to the above subscription
Marain_EnvironmentSuffix|<REPLACE_ME>| This will form the suffix of the naming convention used when creating resources (e.g. 'dev', 'test', 'prod')

