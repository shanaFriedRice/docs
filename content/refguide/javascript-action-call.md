---
title: "JavaScript Action Call"
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details.
---

{{% alert type="info" %}}
This activity can only be used in nanoflows, not in microflows.
{{% /alert %}}

## 1 Introduction

The JavaScript action call activity can be used to call a [JavaScript action](javascript-actions). Arguments can be passed to the action and the result can be stored in a variable.

## 2 Action Properties

### 2.1 JavaScript action

The JavaScript action that is called by this activity.

### 2.2 Arguments

For each parameter of the JavaScript action you have to supply an argument of the same type. The values of the arguments are expressed using [expressions](expressions).

## 3 Output Properties

### 3.1 Return Type

The return type is the data type of the result of the JavaScript action. The return type is defined by the JavaScript action.

### 3.2 Use return value

Determines if the returned value from the JavaScript action should be stored in a variable.

### 3.2 Variable Name

The result of the JavaScript action will be stored in a variable with this name.
