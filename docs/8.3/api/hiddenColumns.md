---
title: HiddenColumns
metaTitle: HiddenColumns - Plugin - Handsontable Documentation
permalink: /8.3/api/hidden-columns
canonicalUrl: /api/hidden-columns
hotPlugin: true
editLink: false
---

# HiddenColumns

[[toc]]

## Description

The `HiddenColumns` plugin lets you hide columns of your choice by default.

"Hiding a column" means that the hidden column doesn't get rendered.
The `HiddenColumns` plugin doesn't modify the source data, and doesn't participate in data transformation
(the shape of data returned by the `getData*` methods stays intact).

Available `HiddenColumns` plugin settings:
 * `columns`: An array of indexes of columns that are hidden on plugin initialization.
 * `copyPasteEnabled`: When set to `true`, takes hidden columns into account when copying or pasting data.
 * `indicators`: When set to `true`, displays UI markers to indicate the presence of hidden columns.

**Example**  
```js
const container = document.getElementById('example');
const hot = new Handsontable(container, {
  data: getData(),
  hiddenColumns: {
    copyPasteEnabled: true,
    indicators: true,
    columns: [1, 2, 5]
  }
});

// access to hiddenColumns plugin instance:
const hiddenColumnsPlugin = hot.getPlugin('hiddenColumns');

// show single column
hiddenColumnsPlugin.showColumn(1);

// show multiple columns
hiddenColumnsPlugin.showColumn(1, 2, 9);

// or as an array
hiddenColumnsPlugin.showColumns([1, 2, 9]);

// hide single column
hiddenColumnsPlugin.hideColumn(1);

// hide multiple columns
hiddenColumnsPlugin.hideColumn(1, 2, 9);

// or as an array
hiddenColumnsPlugin.hideColumns([1, 2, 9]);

// rerender the table to see all changes
hot.render();
```

## Options

### hiddenColumns
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/dataMap/metaManager/metaSchema.js#L2834

:::

_hiddenColumns.hiddenColumns : boolean | object_

The `hiddenColumns` option enables and configures the [HiddenColumns](#hiddencolumns) plugin.

To enable the `HiddenColumns` plugin, set the `hiddenColumns` option to `true`.

To enable the `HiddenColumns` plugin and configure its settings, set the `hiddenColumns` option to an object with the following properties:
 * `columns`: An array of indexes of columns that are hidden on plugin initialization.
 * `copyPasteEnabled`: When set to `true`, takes hidden columns into account when copying or pasting data.
 * `indicators`: When set to `true`, displays UI markers to indicate the presence of hidden columns.

**Default**: <code>undefined</code>  
**Example**  
```js
// enable the `HiddenColumns` plugin
hiddenColumns: true,

// or enable `HiddenColumns` plugin, and configure its settings
hiddenColumns: {
  // set columns that are hidden by default
  columns: [5, 10, 15],
  // take hidden columns into account when copying or pasting
  copyPasteEnabled: true,
  // show where hidden columns are
  indicators: true
}
```

## Methods

### destroy
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L475

:::

_hiddenColumns.destroy()_

Destroys the plugin instance.



### disablePlugin
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L155

:::

_hiddenColumns.disablePlugin()_

Disables the plugin functionality for this Handsontable instance.



### enablePlugin
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L114

:::

_hiddenColumns.enablePlugin()_

Enables the plugin functionality for this Handsontable instance.



### getHiddenColumns
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L267

:::

_hiddenColumns.getHiddenColumns() ⇒ Array&lt;number&gt;_

Returns an array of visual indexes of hidden columns.



### hideColumn
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L258

:::

_hiddenColumns.hideColumn(...column)_

Hides a single column.


| Param | Type | Description |
| --- | --- | --- |
| ...column | `number` | Visual column index. |



### hideColumns
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L225

:::

_hiddenColumns.hideColumns(columns)_

Hides the columns provided in the array.


| Param | Type | Description |
| --- | --- | --- |
| columns | `Array<number>` | Array of visual column indexes. |



### isEnabled
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L107

:::

_hiddenColumns.isEnabled() ⇒ boolean_

Checks if the plugin is enabled in the handsontable settings. This method is executed in [Hooks#beforeInit](@/api/hooks.md#beforeinit)
hook and if it returns `true` than the [HiddenColumns#enablePlugin](@/api/hiddenColumns.md#enableplugin) method is called.



### isHidden
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L279

:::

_hiddenColumns.isHidden(column) ⇒ boolean_

Checks if the provided column is hidden.


| Param | Type | Description |
| --- | --- | --- |
| column | `number` | Visual column index. |



### isValidConfig
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L289

:::

_hiddenColumns.isValidConfig(hiddenColumns) ⇒ boolean_

Get if trim config is valid. Check whether all of the provided column indexes are within the bounds of the table.


| Param | Type | Description |
| --- | --- | --- |
| hiddenColumns | `Array` | List of hidden column indexes. |



### showColumn
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L216

:::

_hiddenColumns.showColumn(...column)_

Shows a single column.


| Param | Type | Description |
| --- | --- | --- |
| ...column | `number` | Visual column index. |



### showColumns
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L168

:::

_hiddenColumns.showColumns(columns)_

Shows the provided columns.


| Param | Type | Description |
| --- | --- | --- |
| columns | `Array<number>` | Array of visual column indexes. |



### updatePlugin
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/hiddenColumns/hiddenColumns.js#L145

:::

_hiddenColumns.updatePlugin()_

Updates the plugin state. This method is executed when [Core#updateSettings](@/api/core.md#updatesettings) is invoked.

