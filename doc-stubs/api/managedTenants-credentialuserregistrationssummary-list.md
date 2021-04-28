---
title: "List credentialUserRegistrationsSummaries"
description: "Get a list of the credentialUserRegistrationsSummary objects and their properties."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: apiPageType
---

# List credentialUserRegistrationsSummaries
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Reports.Read.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /credentialUserRegistrationsSummaries
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

If successful, this method returns a `200 OK` response code and a collection of [credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_credentialuserregistrationssummary"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/credentialUserRegistrationsSummaries
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.management.services.api.credentialUserRegistrationsSummary)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.management.services.api.credentialUserRegistrationsSummary",
      "id": "6f76b50b-b50b-6f76-0bb5-766f0bb5766f",
      "tenantId": "String",
      "tenantDisplayName": "String",
      "mfaAndSsprCapableUserCount": "Integer",
      "ssprEnabledUserCount": "Integer",
      "mfaRegisteredUserCount": "Integer",
      "ssprRegisteredUserCount": "Integer",
      "totalUserCount": "Integer",
      "securityDefaultsEnabled": "Boolean",
      "mfaConditionalAccessPolicyState": "String",
      "lastRefreshedDateTime": "String (timestamp)"
    }
  ]
}
```
