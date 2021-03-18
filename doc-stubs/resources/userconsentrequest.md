---
title: "userConsentRequest resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# userConsentRequest resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [request](../resources/request.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List userConsentRequests](../api/userconsentrequest-list.md)|[userConsentRequest](../resources/userconsentrequest.md) collection|Get a list of the [userConsentRequest](../resources/userconsentrequest.md) objects and their properties.|
|[Create userConsentRequest](../api/userconsentrequest-create.md)|[userConsentRequest](../resources/userconsentrequest.md)|Create a new [userConsentRequest](../resources/userconsentrequest.md) object.|
|[Get userConsentRequest](../api/userconsentrequest-get.md)|[userConsentRequest](../resources/userconsentrequest.md)|Read the properties and relationships of a [userConsentRequest](../resources/userconsentrequest.md) object.|
|[Update userConsentRequest](../api/userconsentrequest-update.md)|[userConsentRequest](../resources/userconsentrequest.md)|Update the properties of a [userConsentRequest](../resources/userconsentrequest.md) object.|
|[Delete userConsentRequest](../api/userconsentrequest-delete.md)|None|Deletes a [userConsentRequest](../resources/userconsentrequest.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdBy|[identitySet](../resources/identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|reason|String|**TODO: Add Description**|
|status|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|approval|[approval](../resources/approval.md)|**TODO: Add Description** Inherited from [request](../resources/request.md)|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userConsentRequest",
  "baseType": "microsoft.graph.request",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userConsentRequest",
  "id": "String (identifier)",
  "reason": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "status": "String",
  "createdDateTime": "String (timestamp)"
}
```

