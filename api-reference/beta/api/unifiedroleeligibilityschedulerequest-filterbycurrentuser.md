---
title: "unifiedRoleEligibilityRequest: filterByCurrentUser"
description: "Get a list of the unifiedRoleEligibilityRequest objects and their properties filtered by a particular user principal"
author: "shauliu"
localization_priority: Normal
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# unifiedRoleEligibilityRequest: filterByCurrentUser
Namespace: microsoft.graph

Get a list of the [unifiedRoleEligibilityRequest](../resources/unifiedroleeligibilityrequest.md) objects and their properties associated with a particular principal object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|PrivilegedAccess.ReadWrite.AzureAD|
|Delegated (personal Microsoft account)|Not supported|
|Application|PrivilegedAccess.Read.AzureAD|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /roleManagement/directory/roleEligibilityRequests/filterByCurrentUser
```

## Function parameters
In the request URL, provide the following query parameters with values.
The following table shows the parameters that can be used with this function.

|Parameter|Type|Description|
|:---|:---|:---|
|on|roleEligibilityRequestFilterByCurrentUserOptions|ID of the principal object|


## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [unifiedRoleEligibilityRequest](../resources/unifiedroleeligibilityrequest.md) collection in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "unifiedroleeligibilityrequest_filterbycurrentuser"
}
-->
``` http
GET https://graph.microsoft.com/beta/roleManagement/directory/roleEligibilityRequests/filterByCurrentUser(on='parameterValue')
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.unifiedRoleEligibilityRequest)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "String (identifier)",
      "action": "String",
      "principalId": "String",
      "roleDefinitionId": "String",
      "directoryScopeId": "String",
      "appScopeId": "String",
      "isValidationOnly": "Boolean",
      "targetScheduleId": "String",
      "justification": "String",
      "scheduleInfo": {
        "@odata.type": "microsoft.graph.requestSchedule"
      },
      "ticketInfo": {
        "@odata.type": "microsoft.graph.ticketInfo"
      }
    }
  ]
}
```

