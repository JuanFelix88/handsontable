---
title: CreatePriorityMap
metaTitle: CreatePriorityMap - API Reference - Handsontable Documentation
permalink: /8.2/api/create-priority-map
canonicalUrl: /api/create-priority-map
hotPlugin: false
editLink: false
---

# CreatePriorityMap

[[toc]]
## Methods

### addItem
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/utils/dataStructures/priorityMap.js#L38

:::

_createPriorityMap~addItem(priority, item)_

Adds items to priority map. Throws an error if `priority` is not a number or if is already added.


| Param | Type | Description |
| --- | --- | --- |
| priority | `number` | The priority for adding item. |
| item | `*` | The adding item. |



### getItems
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/utils/dataStructures/priorityMap.js#L55

:::

_createPriorityMap~getItems([order]) ⇒ \*_

Gets items from the passed map in a ASC or DESC order of priorities.


| Param | Type | Description |
| --- | --- | --- |
| [order] | `string` | `optional` The order for getting items. ASC is an default. |

