# ![LOGO](logo.png) AdvisorManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the AdvisorManagementClient API (version 2017-04-19).

Generated from: https://api.apis.guru/v2/specs/azure.com/advisor/2017-04-19/swagger.json<br/>
Generated at: 2019-05-07T17:37:06+03:00

## API Description

REST APIs for Azure Advisor

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists all the available Advisor REST API operations.

*Tags:* `Operations`

#### Input Parameters
* `api-version` - _required_ - The version of the API to be used with the client request.

### Retrieve Azure Advisor configurations.

> Retrieve Azure Advisor configurations and also retrieve configurations of contained resource groups.

*Tags:* `Configurations`

#### Input Parameters
* `api-version` - _required_ - The version of the API to be used with the client request.
* `subscriptionId` - _required_ - The Azure subscription ID.

### Create/Overwrite Azure Advisor configuration.

> Create/Overwrite Azure Advisor configuration and also delete all configurations of contained resource groups.

*Tags:* `Configurations`

#### Input Parameters
* `api-version` - _required_ - The version of the API to be used with the client request.
* `subscriptionId` - _required_ - The Azure subscription ID.

### Initiates the recommendation generation or computation process for a subscription. This operation is asynchronous. The generated recommendations are stored in a cache in the Advisor service.

*Tags:* `GenerateRecommendations`

#### Input Parameters
* `subscriptionId` - _required_ - The Azure subscription ID.
* `api-version` - _required_ - The version of the API to be used with the client request.

### Retrieves the status of the recommendation computation or generation process. Invoke this API after calling the generation recommendation. The URI of this API is returned in the Location field of the response header.

*Tags:* `GenerateRecommendations`

#### Input Parameters
* `subscriptionId` - _required_ - The Azure subscription ID.
* `operationId` - _required_ - The operation ID, which can be found from the Location field in the generate recommendation response header.
* `api-version` - _required_ - The version of the API to be used with the client request.

### Obtains cached recommendations for a subscription. The recommendations are generated or computed by invoking generateRecommendations.

*Tags:* `GetRecommendations`

#### Input Parameters
* `subscriptionId` - _required_ - The Azure subscription ID.
* `api-version` - _required_ - The version of the API to be used with the client request.
* `$filter` - _optional_ - The filter to apply to the recommendations.
* `$top` - _optional_ - The number of recommendations per page if a paged version of this API is being used.
* `$skipToken` - _optional_ - The page-continuation token to use with a paged version of this API.

### Retrieves the list of snoozed or dismissed suppressions for a subscription. The snoozed or dismissed attribute of a recommendation is referred to as a suppression.

*Tags:* `Suppressions`

#### Input Parameters
* `subscriptionId` - _required_ - The Azure subscription ID.
* `api-version` - _required_ - The version of the API to be used with the client request.
* `$top` - _optional_ - The number of suppressions per page if a paged version of this API is being used.
* `$skipToken` - _optional_ - The page-continuation token to use with a paged version of this API.

### Retrieve Azure Advisor configurations.

*Tags:* `Configurations`

#### Input Parameters
* `api-version` - _required_ - The version of the API to be used with the client request.
* `subscriptionId` - _required_ - The Azure subscription ID.
* `resourceGroup` - _required_ - The name of the Azure resource group.

### Create/Overwrite Azure Advisor configuration.

*Tags:* `Configurations`

#### Input Parameters
* `api-version` - _required_ - The version of the API to be used with the client request.
* `subscriptionId` - _required_ - The Azure subscription ID.
* `resourceGroup` - _required_ - The name of the Azure resource group.

### Obtains details of a cached recommendation.

*Tags:* `GetRecommendations`

#### Input Parameters
* `resourceUri` - _required_ - The fully qualified Azure Resource Manager identifier of the resource to which the recommendation applies.
* `recommendationId` - _required_ - The recommendation ID.
* `api-version` - _required_ - The version of the API to be used with the client request.

### Enables the activation of a snoozed or dismissed recommendation. The snoozed or dismissed attribute of a recommendation is referred to as a suppression.

*Tags:* `Suppressions`

#### Input Parameters
* `resourceUri` - _required_ - The fully qualified Azure Resource Manager identifier of the resource to which the recommendation applies.
* `recommendationId` - _required_ - The recommendation ID.
* `name` - _required_ - The name of the suppression.
* `api-version` - _required_ - The version of the API to be used with the client request.

### Obtains the details of a suppression.

*Tags:* `Suppressions`

#### Input Parameters
* `resourceUri` - _required_ - The fully qualified Azure Resource Manager identifier of the resource to which the recommendation applies.
* `recommendationId` - _required_ - The recommendation ID.
* `name` - _required_ - The name of the suppression.
* `api-version` - _required_ - The version of the API to be used with the client request.

### Enables the snoozed or dismissed attribute of a recommendation. The snoozed or dismissed attribute is referred to as a suppression. Use this API to create or update the snoozed or dismissed status of a recommendation.

*Tags:* `Suppressions`

#### Input Parameters
* `resourceUri` - _required_ - The fully qualified Azure Resource Manager identifier of the resource to which the recommendation applies.
* `recommendationId` - _required_ - The recommendation ID.
* `name` - _required_ - The name of the suppression.
* `api-version` - _required_ - The version of the API to be used with the client request.

## License

**flow**ground :- Telekom iPaaS / azure-com-advisor-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
