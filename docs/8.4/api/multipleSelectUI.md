---
title: MultipleSelectUI
metaTitle: MultipleSelectUI - API Reference - Handsontable Documentation
permalink: /8.4/api/multiple-select-ui
canonicalUrl: /api/multiple-select-ui
hotPlugin: false
editLink: false
---

# MultipleSelectUI

[[toc]]
## Members

### clearAllUI
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L55

:::

_multipleSelectUI.clearAllUI : BaseUI_

"Clear" UI element.



### items
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L64

:::

_multipleSelectUI.items : Array_

List of available select options.



### itemsBox
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L70

:::

_multipleSelectUI.itemsBox : [Handsontable](@/api/core.md)_

Handsontable instance used as items list element.



### searchInput
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L37

:::

_multipleSelectUI.searchInput : [InputUI](@/api/inputUI.md)_

Input element.



### selectAllUI
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L46

:::

_multipleSelectUI.selectAllUI : BaseUI_

"Select all" UI element.


## Methods

### build
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L128

:::

_multipleSelectUI.build()_

Build DOM structure.



### destroy
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L203

:::

_multipleSelectUI.destroy()_

Destroy instance.



### getItems
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L103

:::

_multipleSelectUI.getItems() ⇒ Array_

Get all available options.



### getValue
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L112

:::

_multipleSelectUI.getValue() ⇒ Array_

Get element value.


**Returns**: `Array` - Array of selected values.  

### isSelectedAllValues
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L121

:::

_multipleSelectUI.isSelectedAllValues() ⇒ boolean_

Check if all values listed in element are selected.



### registerHooks
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L78

:::

_multipleSelectUI.registerHooks()_

Register all necessary hooks.



### reset
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L182

:::

_multipleSelectUI.reset()_

Reset DOM structure.



### setItems
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L90

:::

_multipleSelectUI.setItems(items)_

Set available options.


| Param | Type | Description |
| --- | --- | --- |
| items | `Array` | Array of objects with `checked` and `label` property. |



### update
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/filters/ui/multipleSelect.js#L191

:::

_multipleSelectUI.update()_

Update DOM structure.

