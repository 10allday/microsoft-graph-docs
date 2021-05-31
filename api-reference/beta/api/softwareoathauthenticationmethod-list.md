---
title: "List softwareOathAuthenticationMethods"
description: "Retrieve a list of a user's softwareOathAuthenticationMethods objects and their properties."
author: "mmcla"
localization_priority: Normal
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# List softwareOathAuthenticationMethods
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve a list of a user's [Software OATH authentication method](../resources/softwareoathauthenticationmethod.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions acting on self (from least to most privileged)|Permissions acting on others (from least to most privileged)|
|:---|:---|:--|
| Delegated (work or school account)     | UserAuthenticationMethod.ReadWrite | UserAuthenticationMethod.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. | Not supported. |
| Application                            | Not applicable. | UserAuthenticationMethod.ReadWrite.All |

For delegated scenarios where an admin is acting on another user, the admin needs one of the following [roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):

* Global admin
* Privileged authentication admin
* Authentication admin

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/authentication/softwareOathAuthenticationMethods
GET /users/{id | userPrincipalName}/authentication/softwareOathAuthenticationMethods
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

If successful, this method returns a `200 OK` response code and a collection of [softwareOathAuthenticationMethod](../resources/softwareoathauthenticationmethod.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_softwareoathauthenticationmethod"
}
-->
``` http
GET https://graph.microsoft.com/beta/me/authentication/softwareOathMethods
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.softwareOathAuthenticationMethod)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.softwareOathAuthenticationMethod",
      "id": "b172893e-893e-b172-3e89-72b13e8972b1",
      "secretKey": "String"
    }
  ]
}
```

