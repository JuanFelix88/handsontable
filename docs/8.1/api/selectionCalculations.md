---
title: SelectionCalculations
metaTitle: SelectionCalculations - Plugin - Handsontable Documentation
permalink: /8.1/api/selection-calculations
canonicalUrl: /api/selection-calculations
hotPlugin: true
editLink: false
---

# SelectionCalculations

[[toc]]

## Description

Class responsible for all of the Selection-related operations on merged cells.


## Members

### fullySelectedMergedCellClassName
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L23

:::

_selectionCalculations.fullySelectedMergedCellClassName : string_

Class name used for fully selected merged cells.



### plugin
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L17

:::

_selectionCalculations.plugin : [MergeCells](@/api/mergeCells.md)_

Reference to the Merge Cells plugin.


## Methods

### getSelectedMergedCellClassName
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L116

:::

_selectionCalculations.getSelectedMergedCellClassName(currentRow, currentColumn, cornersOfSelection, layerLevel) ⇒ string | undefined_

Generate an additional class name for the entirely-selected merged cells.


| Param | Type | Description |
| --- | --- | --- |
| currentRow | `number` | Visual row index of the currently processed cell. |
| currentColumn | `number` | Visual column index of the currently cell. |
| cornersOfSelection | `Array` | Array of the current selection in a form of `[startRow, startColumn, endRow, endColumn]`. |
| layerLevel | `number` <br/> `undefined` | Number indicating which layer of selection is currently processed. |


**Returns**: `string` | `undefined` - A `String`, which will act as an additional `className` to be added to the currently processed cell.  

### getSelectedMergedCellClassNameToRemove
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L194

:::

_selectionCalculations.getSelectedMergedCellClassNameToRemove() ⇒ Array&lt;string&gt;_

Generate an array of the entirely-selected merged cells' class names.


**Returns**: `Array<string>` - An `Array` of `String`s. Each of these strings will act like class names to be removed from all the cells in the table.  

### getUpdatedSelectionRange
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L99

:::

_selectionCalculations.getUpdatedSelectionRange(oldSelectionRange, delta) ⇒ [CellRange](@/api/cellRange.md)_

Get a selection range with `to` property incremented by the provided delta.


| Param | Type | Description |
| --- | --- | --- |
| oldSelectionRange | `CellRange` | The base selection range. |
| delta | `object` | The delta object with `row` and `col` properties. |


**Returns**: [`CellRange`](@/api/cellRange.md) - A new `CellRange` object.  

### isMergeCellFullySelected
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L161

:::

_selectionCalculations.isMergeCellFullySelected(mergedCell, selectionRangesArray) ⇒ boolean_

Check if the provided merged cell is fully selected (by one or many layers of selection).


| Param | Type | Description |
| --- | --- | --- |
| mergedCell | `MergedCellCoords` | The merged cell to be processed. |
| selectionRangesArray | `Array<CellRange>` | Array of selection ranges. |



### snapDelta
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/mergeCells/calculations/selection.js#L35

:::

_selectionCalculations.snapDelta(delta, selectionRange, mergedCell)_

"Snap" the delta value according to defined merged cells. (In other words, compensate the rowspan -
e.g. Going up with `delta.row = -1` over a merged cell with `rowspan = 3`, `delta.row` should change to `-3`.).


| Param | Type | Description |
| --- | --- | --- |
| delta | `object` | The delta object containing `row` and `col` properties. |
| selectionRange | `CellRange` | The selection range. |
| mergedCell | `object` | A merged cell object. |

