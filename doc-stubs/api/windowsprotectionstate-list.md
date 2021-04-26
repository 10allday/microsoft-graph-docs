---
title: "List windowsProtectionStates"
description: "Get a list of the windowsProtectionState objects and their properties."
author: isaiahwilliams
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List windowsProtectionStates
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [windowsProtectionState](../resources/windowsprotectionstate.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementManagedDevices.Read.All, DeviceManagementManagedDevices.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /windowsProtectionStates
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

If successful, this method returns a `200 OK` response code and a collection of [windowsProtectionState](../resources/windowsprotectionstate.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_windowsprotectionstate"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/windowsProtectionStates
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.management.services.api.windowsProtectionState)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.management.services.api.windowsProtectionState",
      "id": "faf85df2-5df2-faf8-f25d-f8faf25df8fa",
      "tenantId": "String",
      "tenantDisplayName": "String",
      "managedDeviceId": "String",
      "managedDeviceName": "String",
      "malwareProtectionEnabled": "Boolean",
      "managedDeviceHealthState": "String",
      "realTimeProtectionEnabled": "Boolean",
      "networkInspectionSystemEnabled": "Boolean",
      "quickScanOverdue": "Boolean",
      "fullScanOverdue": "Boolean",
      "signatureUpdateOverdue": "Boolean",
      "rebootRequired": "Boolean",
      "attentionRequired": "Boolean",
      "fullScanRequired": "Boolean",
      "engineVersion": "String",
      "signatureVersion": "String",
      "antiMalwareVersion": "String",
      "lastQuickScanDateTime": "String (timestamp)",
      "lastFullScanDateTime": "String (timestamp)",
      "lastQuickScanSignatureVersion": "String",
      "lastFullScanSignatureVersion": "String",
      "lastReportedDateTime": "String (timestamp)",
      "devicePropertiesRefreshTime": "String (timestamp)",
      "deviceDeleted": "Boolean",
      "lastRefreshedDateTime": "String (timestamp)"
    }
  ]
}
```

