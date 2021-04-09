---
title: "Get hostedContent in an app's icon"
description: "Retrieve the hosted content in a teamsAppIcon."
localization_priority: Normal
author: "jecha"
ms.prod: "microsoft-teams"
doc_type: "apiPageType"
---

# Get hostedContent in an app's icon

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve the [hosted content](../resources/teamworkhostedcontent.md) in an [app's icon](../resources/teamsappicon.md).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission Type                        | Permissions (from least to most privileged)                      |
| :------------------------------------- | :--------------------------------------------------------------- |
| Delegated (work or school account)     | AppCatalog.Read.All, AppCatalog.ReadWrite.All, AppCatalog.Submit |
| Delegated (personal Microsoft account) | Not supported.                                                   |
| Application                            | Not supported.                                                   |

## HTTP request

**Get hosted content in app icon**

<!-- { "blockType": "ignored" } -->
```http
GET /appCatalogs/teamsApps/{teams-app-id}/appDefinitions/{app-definition-id}/colorIcon/hostedContent/
GET /appCatalogs/teamsApps/{teams-app-id}/appDefinitions/{app-definition-id}/outlineIcon/hostedContent/
```

## Optional query parameters

This operation supports the `$select` [OData query parameters](/graph/query-parameter) to customize the response.

## Request headers

| Header           | Value                      |
| :--------------- | :------------------------- |
| Authorization    | Bearer {token}. Required.  |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [teamworkHostedContent](../resources/teamworkhostedcontent.md) object in the response body.

## Examples

### Example 1: Get hosted content in color icon.

#### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "teamsappicon_get_hostedcontent"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps/5a31d4f7-a11d-4052-96eb-1b40786a2a78/appDefinitions/NWEzMWQ0ZjctYTExZC00MDUyLTk2ZWItMWI0MDc4NmEyYTc4IyM2LjAuNSMjUHVibGlzaGVk/colorIcon/hostedContent/
```

---

#### Response

The following example shows the response.

> **Note:** `contentBytes` and `contentType` are always set to null.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamworkHostedContent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#appCatalogs/teamsApps('5a31d4f7-a11d-4052-96eb-1b40786a2a78')/appDefinitions('NWEzMWQ0ZjctYTExZC00MDUyLTk2ZWItMWI0MDc4NmEyYTc4IyM2LjAuNSMjUHVibGlzaGVk')/colorIcon/hostedContent/$entity",
    "id": "aWQ9LHR5cGU9MSx1cmw9aHR0cHM6Ly91cy1hcGkuYXNtLnNreXBlLmNvbS92MS9vYmplY3RzLzAtd3VzLWQ0LWQwOGVkNTQ2MjQ2MTliNTc4OGIwMWUzODNlMWVjYzU3L3ZpZXdzL2ltZ3BzaF9mdWxsc2l6ZQ==",
    "contentBytes": null,
    "contentType": null
}
```

---

### Example 2: Get hosted content's image in outline icon.

#### Request

The following is an example of the request.

> **Note:** Requests for the raw value does not support [OData query parameters](/graph/query-parameters) to customize the response.

<!-- {
  "blockType": "request",
  "name": "teamsappicon_get_hostedcontentbytes"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps/5a31d4f7-a11d-4052-96eb-1b40786a2a78/appDefinitions/NWEzMWQ0ZjctYTExZC00MDUyLTk2ZWItMWI0MDc4NmEyYTc4IyM2LjAuNSMjUHVibGlzaGVk/outlineIcon/hostedContent/$value
```

---

#### Response

Response contains bytes for the hosted content in the body. `content-type` header specifies the kind of hosted content.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamworkHostedContent"
} -->
```http
HTTP/1.1 200 OK
Content-type: image/png
```