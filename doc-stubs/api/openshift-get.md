---
title: "Get openShift"
description: "Read the properties and relationships of an openShift object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get openShift
Namespace: microsoft.graph



Read the properties and relationships of an [openShift](../resources/openshift.md) object.

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
GET /teams/{teamsId}/schedule/openShifts/{openShiftId}
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

If successful, this method returns a `200 OK` response code and an [openShift](../resources/openshift.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_openshift"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/teams/{teamsId}/schedule/openShifts/{openShiftId}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.openShift"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.openShift",
    "id": "3d4b4d3c-4d3c-3d4b-3c4d-4b3d3c4d4b3d",
    "createdBy": {
      "@odata.type": "microsoft.graph.identitySet"
    },
    "createdDateTime": "String (timestamp)",
    "lastModifiedBy": {
      "@odata.type": "microsoft.graph.identitySet"
    },
    "lastModifiedDateTime": "String (timestamp)",
    "draftOpenShift": {
      "@odata.type": "microsoft.graph.openShiftItem"
    },
    "isStagedForDeletion": "Boolean",
    "schedulingGroupId": "String",
    "sharedOpenShift": {
      "@odata.type": "microsoft.graph.openShiftItem"
    }
  }
}
```

