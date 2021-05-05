---
title: Undo and redo
permalink: /next/undo-redo
canonicalUrl: /undo-redo
tags:
  - history of changes
  - state history
  - stack update
  - repeat
  - reverse
  - erase last change
  - roll back changes
---

# Undo and redo

[[toc]]

## Overview

This feature allows you to revert changes made in the data grid. It is very useful in a normal day-to-day routine, especially when the change is unintentional. This feature stacks the changes made with the user interface of the grid. Modifications done programatically are ommitted.

The basic methods are `undo()` and `redo()`. The `undo()` method rolls back the last performed action, and the `undo()` restores it.

This feature is provided by the `undoRedo` plugin, and is enabled by default.

:::tip
Not all user-triggered actions are covered by this feature. See the below list of actions that won't be added to the history of changes:

- Sort
- Filter
- Move column
- Move row
:::

## Basic demo

Make some changes to the grid below and the use the <kbd>Ctrl/⌘Cmd + Z</kbd> command to redo the previous state. Then, use <kbd>Ctrl/⌘ Cmd + Y</kbd> to restore it.

::: example #example
```javascript
var example = document.getElementById('example');
var hot1 = new Handsontable(example, {
 data: Handsontable.helper.createSpreadsheetData(10, 5),
 rowHeaders: true,
 colHeaders: true,
 stretchH: 'all',
 licenseKey: 'non-commercial-and-evaluation'
});
```
:::