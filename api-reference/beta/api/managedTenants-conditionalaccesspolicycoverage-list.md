---
title: "List conditionalAccessPolicyCoverages"
description: "Get a list of the conditionalAccessPolicyCoverage objects and their properties."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: apiPageType
---

# List conditionalAccessPolicyCoverages
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Policy.Read.All, Policy.ReadWrite.ConditionalAccess, Application.Read.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /conditionalAccessPolicyCoverages
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_conditionalaccesspolicycoverage"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenant/conditionalAccessPolicyCoverages
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.management.services.api.conditionalAccessPolicyCoverage)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.management.services.api.conditionalAccessPolicyCoverage",
      "id": "baa2983f-983f-baa2-3f98-a2ba3f98a2ba",
      "tenantDisplayName": "String",
      "conditionalAccessPolicyState": "String",
      "requiresDeviceCompliance": "Boolean",
      "latestPolicyModifiedDateTime": "String (timestamp)"
    }
  ]
}
```
