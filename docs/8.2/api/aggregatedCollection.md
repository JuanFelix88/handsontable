---
title: AggregatedCollection
metaTitle: AggregatedCollection - API Reference - Handsontable Documentation
permalink: /8.2/api/aggregated-collection
canonicalUrl: /api/aggregated-collection
hotPlugin: false
editLink: false
---

# AggregatedCollection

[[toc]]
## Members

### aggregationFunction
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L21

:::

_aggregatedCollection.aggregationFunction_

Function which do aggregation on the values for particular index.



### fallbackValue
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L25

:::

_aggregatedCollection.fallbackValue_

Fallback value when there is no calculated value for particular index.



### mergedValuesCache
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L17

:::

_aggregatedCollection.mergedValuesCache : Array_

List of merged values. Value for each index is calculated using values inside registered maps.


## Methods

### getMergedValueAtIndex
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L92

:::

_aggregatedCollection.getMergedValueAtIndex(index, [readFromCache]) ⇒ \*_

Get merged value for particular index.


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| index | `number` |  | Index for which we calculate single result. |
| [readFromCache] | `boolean` | <code>true</code> | `optional` Determine if read results from the cache. |



### getMergedValues
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L34

:::

_aggregatedCollection.getMergedValues([readFromCache]) ⇒ Array_

Get merged values for all indexes.


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [readFromCache] | `boolean` | <code>true</code> | `optional` Determine if read results from the cache. |



### updateCache
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/translations/mapCollections/aggregatedCollection.js#L101

:::

_aggregatedCollection.updateCache()_

Rebuild cache for the collection.

