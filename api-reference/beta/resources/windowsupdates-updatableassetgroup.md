---
title: "updatableAssetGroup resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# updatableAssetGroup resource type

Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A group of updatable assets. An azureADDevice can be a member; an updatable asset group cannot be a member.


Inherits from [updatableAsset](../resources/windowsupdates-updatableasset.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List updatableAssetGroups](../api/windowsupdates-updatableassetgroup-list.md)|[updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md) collection|Get a list of the [updatableAssetGroup](../resources/updatableassetgroup.md) objects and their properties.|
|[Create updatableAssetGroup](../api/windowsupdates-updatableassetgroup-create.md)|[updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md)|Create a new [updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md) object.|
|[Get updatableAssetGroup](../api/windowsupdates-updatableassetgroup-get.md)|[updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md)|Read the properties and relationships of an [updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md) object.|
|[Delete updatableAssetGroup](../api/windowsupdates-updatableassetgroup-delete.md)|None|Deletes an [updatableAssetGroup](../resources/windowsupdates-updatableassetgroup.md) object.|
|[Add members](../api/windowsupdates-updatableassetgroup-addmembers.md)|None|Add members to an updatable asset group.|
|[Remove members](../api/windowsupdates-updatableassetgroup-removemembers.md)|None|Remove members from an updatable asset group.|
|[List members](../api/windowsupdates-updatableassetgroup-list-members.md)|[updatableAsset](../resources/windowsupdates-updatableasset.md) collection|Get the updatableAsset resources from the members navigation property.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|An identifier for the group. Key. Not nullable. Read-only. Returned by default. Inherited from [updatableAsset](../resources/windowsupdates-updatableasset.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|members|[updatableAsset](../resources/windowsupdates-updatableasset.md) collection|Members of the group. Read-only.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUpdates.updatableAssetGroup",
  "baseType": "microsoft.graph.windowsUpdates.updatableAsset",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdates.updatableAssetGroup",
  "id": "String (identifier)"
}
```

