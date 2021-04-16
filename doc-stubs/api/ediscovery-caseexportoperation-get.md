---
title: "Get caseExportOperation"
description: "Read the properties and relationships of a caseExportOperation object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get caseExportOperation
Namespace: microsoft.graph.ediscovery



Read the properties and relationships of a [caseExportOperation](../resources/ediscovery-caseexportoperation.md) object.

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
GET /caseExportOperation
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

If successful, this method returns a `200 OK` response code and a [caseExportOperation](../resources/ediscovery-caseexportoperation.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_caseexportoperation"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/caseExportOperation
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.ediscovery.caseExportOperation"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.ediscovery.caseExportOperation",
    "id": "116b89c0-89c0-116b-c089-6b11c0896b11",
    "action": "String",
    "completedDateTime": "String (timestamp)",
    "createdBy": {
      "@odata.type": "microsoft.graph.identitySet"
    },
    "createdDateTime": "String (timestamp)",
    "percentProgress": "Integer",
    "resultInfo": {
      "@odata.type": "microsoft.graph.resultInfo"
    },
    "status": "String",
    "azureBlobContainer": "String",
    "azureBlobToken": "String",
    "description": "String",
    "exportOptions": "String",
    "exportStructure": "String",
    "outputFolderId": "String",
    "outputName": "String"
  }
}
```

