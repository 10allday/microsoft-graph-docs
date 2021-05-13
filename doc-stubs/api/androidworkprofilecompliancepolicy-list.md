---
title: "List androidWorkProfileCompliancePolicies"
description: "Get a list of the androidWorkProfileCompliancePolicy objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List androidWorkProfileCompliancePolicies
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [androidWorkProfileCompliancePolicy](../resources/androidworkprofilecompliancepolicy.md) objects and their properties.

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
GET ** Collection URI for microsoft.graph.androidWorkProfileCompliancePolicy not found
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

If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileCompliancePolicy](../resources/androidworkprofilecompliancepolicy.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_androidworkprofilecompliancepolicy"
}
-->
``` http
GET https://graph.microsoft.com/beta** Collection URI for microsoft.graph.androidWorkProfileCompliancePolicy not found
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.androidWorkProfileCompliancePolicy)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
      "id": "06268844-8844-0626-4488-260644882606",
      "roleScopeTagIds": [
        "String"
      ],
      "createdDateTime": "String (timestamp)",
      "description": "String",
      "lastModifiedDateTime": "String (timestamp)",
      "displayName": "String",
      "version": "Integer",
      "passwordRequired": "Boolean",
      "passwordMinimumLength": "Integer",
      "passwordRequiredType": "String",
      "passwordMinutesOfInactivityBeforeLock": "Integer",
      "passwordExpirationDays": "Integer",
      "passwordPreviousPasswordBlockCount": "Integer",
      "passwordSignInFailureCountBeforeFactoryReset": "Integer",
      "securityPreventInstallAppsFromUnknownSources": "Boolean",
      "securityDisableUsbDebugging": "Boolean",
      "securityRequireVerifyApps": "Boolean",
      "deviceThreatProtectionEnabled": "Boolean",
      "deviceThreatProtectionRequiredSecurityLevel": "String",
      "advancedThreatProtectionRequiredSecurityLevel": "String",
      "securityBlockJailbrokenDevices": "Boolean",
      "osMinimumVersion": "String",
      "osMaximumVersion": "String",
      "minAndroidSecurityPatchLevel": "String",
      "storageRequireEncryption": "Boolean",
      "securityRequireSafetyNetAttestationBasicIntegrity": "Boolean",
      "securityRequireSafetyNetAttestationCertifiedDevice": "Boolean",
      "securityRequireGooglePlayServices": "Boolean",
      "securityRequireUpToDateSecurityProviders": "Boolean",
      "securityRequireCompanyPortalAppIntegrity": "Boolean",
      "securityRequiredAndroidSafetyNetEvaluationType": "String"
    }
  ]
}
```

