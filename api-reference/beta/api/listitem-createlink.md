---
title: "listItem: createLink"
description: "You can use createLink action to share a ListItem via a sharing link."
author: "learafa"
localization_priority: Normal
ms.prod: "sharepoint"
doc_type: apiPageType
---

# listItem: createLink

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

You can use **createLink** action to share a [ListItem](../resources/listitem.md) via a sharing link.

The **createLink** action will create a new sharing link if the specified link type doesn't already exist for the calling application.
If a sharing link of the specified type already exists for the app, the existing sharing link will be returned.

ListItem resources inherit sharing permissions from their ancestors.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegated (personal Microsoft account) | Files.ReadWrite, Files.ReadWrite.All    |
|Application | Files.ReadWrite.All, Sites.ReadWrite.All |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /sites/{siteId}/lists/{listId}/items/{itemId}/createLink
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Parameter|Type|Description|
|:---|:---|:---|
|type|String|Optional.Optional.The type of sharing link to create. |
|scope|String|Optional. The scope of link to create. Either anonymous, organization or users.|
|expirationDateTime|DateTimeOffset|Optional. A String with format of yyyy-MM-ddTHH:mm:ssZ of DateTime indicates the expiration time of the permission.|
|password|String|Optional.The password of the sharing link that is set by the creator.|
|recipients|[driveRecipient](../resources/driverecipient.md) collection|Optional. A collection of recipients who will receive access to the sharing link.|

### Link types

The following values are allowed for the **type** parameter.

| Type value | Description                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| view           | Creates a read-only link to the Item.                                                                        |
| review         | Creates a review link to the Item. This option is only available for files in OneDrive for Business and SharePoint.                   |
| edit           | Creates an read-write link to the Item.                                                                       |
| embed          | Creates an embeddable link to the Item.                                                                      |
| blocksDownload | Creates a read-only link that blocks download to the Item. This option is only available for files in OneDrive for Business and SharePoint.  |
| createOnly     | Creates an upload-only link to the Item. This option is only available for folders in OneDrive for Business and SharePoint.             |
| addressBar     | Gets the admin-allowed address bar link to the Item. Only available in OneDrive for Business and SharePoint. The organization admin configures whether this link type is supported, and what features are supported by this link type. |
| adminDefault   | Creates the default link to the listItem as determined by the administrator of the organization. Only available in OneDrive for Business and SharePoint. The policy is enforced for the organization by the admin |

### Scope types

The following values are allowed for the **scope** parameter.

| Value          | Description
|:---------------|:------------------------------------------------------------
| anonymous    | Anyone with the link has access, without needing to sign in. This may include people outside of your organization. Anonymous link support may be disabled by an administrator.
| organization | Anyone signed into your organization (tenant) can use the link to get access. Only available in OneDrive for Business and SharePoint.
| users        | Specific people in the recipients collection can use the link to get access. Only available in OneDrive for Business and SharePoint.

## Response

If successful, this method returns a single [Permission](../resources/permission.md) resource in the response body that represents the requested sharing permissions.

The response will be `201 Created` if a new sharing link is created for the item or `200 OK` if an existing link is returned.

## Examples

### Create a link to share a drive item
The following example requests a sharing link to be created for the DriveItem specified by {itemId} in the user's OneDrive.
The sharing link is configured to be read-only and usable by anyone with the link.

#### Request
<!-- {
  "blockType": "request",
  "name": "listitem_createlink"
}
-->
``` http
POST /sites/{siteId}/lists/{listId}/items/{itemId}/createLink
Content-Type: application/json
Content-length: 212

{
  "type": "String",
  "scope": "String",
  "expirationDateTime": "String (timestamp)",
  "password": "String",
  "recipients": [
    {
      "@odata.type": "microsoft.graph.driveRecipient"
    }
  ]
}
```

#### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "view",
    "scope": "anonymous",
    "webUrl": "https://1drv.ms/A6913278E564460AA616C71B28AD6EB6",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  },
  "hasPassword": true
}
```

### Creating company sharable links

OneDrive for Business and SharePoint support company sharable links.
These are similar to anonymous links, except they only work for members of the owning organization.
To create a company sharable link, use the **scope** parameter with a value of `organization`.

#### Request

```http
POST /sites/{siteId}/lists/{listId}/items/{itemId}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

#### Response

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "edit",
    "scope": "organization",
    "webUrl": "https://contoso-my.sharepoint.com/personal/ellen_contoso_com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

### Creating embeddable links

When using the `embed` link type, the webUrl returned can be embedded in an `<iframe>` HTML element.
When an embed link is created the `webHtml` property contains the HTML code for an `<iframe>` to host the content.

**Note:** Embed links are only supported for OneDrive personal.

#### Request

```http
POST /sites/{siteId}/lists/{listId}/items/{itemId}/createLink
Content-Type: application/json

{
  "type": "embed"
}
```

#### Response

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["read"],
  "link": {
    "type": "embed",
    "webHtml": "<IFRAME src=\"https://onedrive.live.com/...\"></IFRAME>",
    "webUrl": "https://onedive.live.com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## Remarks

* If both scope and type are not provided, a readily available link is provided based on the callers ability on the item and policy is enforced for the organization.
* Links created using this action do not expire unless a default expiration policy is enforced for the organization.
* Links are visible in the sharing permissions for the item and can be removed by an owner of the item.
* Links always point to the current version of a item unless the item is checked out (SharePoint only).

<!--
{
  "type": "#page.annotation",
  "description": "Create a new sharing link for an item.",
  "keywords": "create,sharing,sharing link",
  "section": "documentation",
  "tocPath": "Sharing/Create link",
  "suppressions": [
  ]
}
-->