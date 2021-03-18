---
title: "Update qrAuthenticationMethodConfiguration"
description: "Update the properties of a qrAuthenticationMethodConfiguration object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update qrAuthenticationMethodConfiguration
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [qrAuthenticationMethodConfiguration](../resources/qrauthenticationmethodconfiguration.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
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
PATCH /qrAuthenticationMethodConfiguration
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [qrAuthenticationMethodConfiguration](../resources/qrauthenticationmethodconfiguration.md) object.

The following table shows the properties that are required when you update the [qrAuthenticationMethodConfiguration](../resources/qrauthenticationmethodconfiguration.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|state|authenticationMethodState|**TODO: Add Description** Inherited from [authenticationMethodConfiguration](../resources/authenticationmethodconfiguration.md). Possible values are: `enabled`, `disabled`.|



## Response

If successful, this method returns a `200 OK` response code and an updated [qrAuthenticationMethodConfiguration](../resources/qrauthenticationmethodconfiguration.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_qrauthenticationmethodconfiguration"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/qrAuthenticationMethodConfiguration
Content-Type: application/json
Content-length: 99

{
  "@odata.type": "#microsoft.graph.qrAuthenticationMethodConfiguration",
  "state": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.qrAuthenticationMethodConfiguration",
  "id": "ea9bcea8-cea8-ea9b-a8ce-9beaa8ce9bea",
  "state": "String"
}
```

