---
title: "qualityUpdateReference resource type"
description: "Represents Windows 10 quality update content."
author: "Alice-at-Microsoft"
localization_priority: Normal
ms.prod: "w10"
doc_type: resourcePageType
---

# qualityUpdateReference resource type

Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents Windows 10 quality update content.

In a deployment, the same quality update reference could result in devices receiving different update revisions, but the content is considered contextually equivalent for all devices in the deployment.


Inherits from [windowsUpdateReference](../resources/windowsupdates-windowsupdatereference.md).

## Properties
|Property|Type|Description|
|:---|:---|:---|
|classification|qualityUpdateClassification|Specifies the classification of the referenced content. Possible values are: `all`, `security`, `nonSecurity`.|
|releaseDate|DateTimeOffset|Specifies a quality update in the given servicingChannel with the given classification by date (i.e. the last update published on the specified date). Default value is security.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdates.qualityUpdateReference"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdates.qualityUpdateReference",
  "classification": "String",
  "releaseDate": "String (timestamp)"
}
```

