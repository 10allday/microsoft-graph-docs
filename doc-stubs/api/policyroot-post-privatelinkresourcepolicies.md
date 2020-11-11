---
title: "Create privateLinkResourcePolicies"
description: "Create a new privateLinkResourcePolicy object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create privateLinkResourcePolicies
Namespace: microsoft.graph

Create a new privateLinkResourcePolicy object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /policyRoot/privateLinkResourcePolicies
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [privateLinkResourcePolicy](../resources/privatelinkresourcepolicy.md) object.

The following table shows the properties that are required when you create the [privateLinkResourcePolicy](../resources/privatelinkresourcepolicy.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description**|
|externalPrivateLinkId|String|**TODO: Add Description**|
|tenantApprovals|[tenantApprovals](../resources/tenantapprovals.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [privateLinkResourcePolicy](../resources/privatelinkresourcepolicy.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_privatelinkresourcepolicy_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/policyRoot/privateLinkResourcePolicies
Content-Type: application/json
Content-length: 217

{
  "@odata.type": "#Microsoft.DirectoryServices.privateLinkResourcePolicy",
  "externalPrivateLinkId": "String",
  "tenantApprovals": [
    {
      "@odata.type": "microsoft.graph.tenantApprovals"
    }
  ]
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Microsoft.DirectoryServices.privateLinkResourcePolicy"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#Microsoft.DirectoryServices.privateLinkResourcePolicy",
  "id": "b31487c5-87c5-b314-c587-14b3c58714b3",
  "externalPrivateLinkId": "String",
  "tenantApprovals": [
    {
      "@odata.type": "microsoft.graph.tenantApprovals"
    }
  ]
}
```
