---
title: DisplaySwitch
metaTitle: DisplaySwitch - Plugin - Handsontable Documentation
permalink: /8.4/api/display-switch
canonicalUrl: /api/display-switch
hotPlugin: true
editLink: false
---

# DisplaySwitch

[[toc]]

## Description

Display switch for the Comments plugin. Manages the time of delayed displaying / hiding comments.


## Members

### hidingTimer
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L34

:::

_displaySwitch.hidingTimer : number_

Reference to timer, run by `setTimeout`, which is hiding comment.



### showDebounced
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L28

:::

_displaySwitch.showDebounced : function_

Show comment after predefined delay. It keeps reference to immutable `debounce` function.



### wasLastActionShow
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L22

:::

_displaySwitch.wasLastActionShow : boolean_

Flag to determine if comment can be showed or hidden. State `true` mean that last performed action
was an attempt to show comment element. State `false` mean that it was attempt to hide comment element.


## Methods

### cancelHiding
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L65

:::

_displaySwitch.cancelHiding()_

Cancel hiding comment.



### destroy
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L88

:::

_displaySwitch.destroy()_

Destroy the switcher.



### hide
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L42

:::

_displaySwitch.hide()_

Responsible for hiding comment after proper delay.



### show
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L57

:::

_displaySwitch.show(range)_

Responsible for showing comment after proper delay.


| Param | Type | Description |
| --- | --- | --- |
| range | `object` | Coordinates of selected cell. |



### updateDelay
  
::: source-code-link https://github.com/handsontable/handsontable/blob/710a3bbf6ce1cb5d45e44290a64929caab01adc6/src/plugins/comments/displaySwitch.js#L77

:::

_displaySwitch.updateDelay(displayDelay)_

Update the switch settings.


| Param | Type | Description |
| --- | --- | --- |
| displayDelay | `number` | Delay of showing the comments (in milliseconds). |

