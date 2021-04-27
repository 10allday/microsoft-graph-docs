---
title: "alterationResponse resource type"
description: "Provides related information of spelling correction in the alteration response."
localization_priority: Normal
author: "nmoreau"
ms.prod: "search"
doc_type: "resourcePageType"
---

# alterationResponse resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Provides related information of spelling correction in the alteration response.

## Properties

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|originalQueryString|String| Defines the original user query string.|
|queryAlteration|[searchAlteration](searchalteration.md)| Defines the details of alteration information for spelling correction.|
|queryAlterationType|[searchAlterationType](enums.md#searchAlterationType)| Defines enum type of [searchAlteration](searchalteration.md) that is applied to query for spelling correction.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alterationResponse",
  "baseType": null
}-->

```json
{
  "originalQueryString": "String",
  "queryAlteration": {"@odata.type": "microsoft.graph.searchAlteration"},
  "queryAlterationType": "suggestion"
}
```