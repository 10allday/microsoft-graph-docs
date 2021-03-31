---
title: "Graph Connector API limits"
description: "Graph Connector API limits"
author: "mecampos"
localization_priority: Priority
ms.author: "mecampos"
ms.prod: "data-inflow"
---

# API limits

To ensure consistent availability and performance for everyone, we apply some limits to how the Connector APIs are used. Please refer to the tables below for the current limits.

## Connection limits

| **Limit** | **Description** |
| --- | --- |
| **10 connections** | The maximum number of connections per Microsoft 365 tenant. |
| --- | --- |
| **700,000 items** | The maximum number of items per connection. |
| **70 GB** | The maximum byte size of a connection. |

## Schema limits

| **Limit** | **Description** |
| --- | --- |
| **128 properties** | The maximum number of properties that can be defined in a schema, characterizing the data ingested through a connection. |
| --- | --- |

## Group limits

| **Limit** | **Description** |
| --- | --- |
| **128 chracters** | The maximum length of the ID string of an external group. Must be unique within a connection. Only alpha-numeric characters are supported. |
| --- | --- |
| **1000 requests/sec** | Group administration APIs throttling. |

## Item ingestion

| **Limit** | **Description** |
| --- | --- |
| **4 items/sec (250 MB/hour)** | The throughput limit to ingest items through a connection. |
| --- | --- |
| **4 MB** | The maximum size of an item; this limit applies to the request body when ingesting and indexing an item. |
| **N/A** | The maximum size of a property. |

## Throttling

When a [throttling](https://docs.microsoft.com/graph/throttling) threshold is exceeded, Microsoft Graph limits any further requests from that client for a period of time. When throttling occurs, Microsoft Graph returns HTTP status code 429 (Too many requests), and the requests fail. A suggested wait time is returned in the response header of the failed request. Throttling behavior can depend on the type and number of requests. For example, if you have a high volume of requests, all requests types are throttled. Threshold limits vary based on the request type. Therefore, you could encounter a scenario where writes are throttled but reads are still permitted.