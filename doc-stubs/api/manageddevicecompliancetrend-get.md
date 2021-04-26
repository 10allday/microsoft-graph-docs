---
title: "Get managedDeviceComplianceTrend"
description: "Read the properties and relationships of a managedDeviceComplianceTrend object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: apiPageType
---

# Get managedDeviceComplianceTrend
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [managedDeviceComplianceTrend](../resources/manageddevicecompliancetrend.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementManagedDevices.Read.All, DeviceManagementManagedDevices.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /managedDeviceComplianceTrends/{managedDeviceComplianceTrendsId}
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

If successful, this method returns a `200 OK` response code and a [managedDeviceComplianceTrend](../resources/manageddevicecompliancetrend.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_manageddevicecompliancetrend"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedDeviceComplianceTrends/{managedDeviceComplianceTrendsId}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.managedDeviceComplianceTrend"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.management.services.api.managedDeviceComplianceTrend",
    "id": "8e84db46-db46-8e84-46db-848e46db848e",
    "tenantId": "String",
    "tenantDisplayName": "String",
    "unknownDeviceCount": "Integer",
    "compliantDeviceCount": "Integer",
    "noncompliantDeviceCount": "Integer",
    "errorDeviceCount": "Integer",
    "inGracePeriodDeviceCount": "Integer",
    "configManagerDeviceCount": "Integer",
    "countDateTime": "String"
  }
}
```
