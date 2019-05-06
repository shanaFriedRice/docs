---
title: "JavaScript Actions"
category: "App Modeling"
description: "Describes using JavaScript Actions to extend the functionality of your Mendix app."
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details.
---

## 1 Introduction

With JavaScript actions you can extend the functionality of your application in situations where it would be hard to implement this functionality in nanoflows. You can call a JavaScript action from a nanoflow using the [JavaScript Action Call](javascript-action-call).

{{% alert type="info" %}}

Each Java action defined in Studio Pro corresponds to a file *{name of JavaScript action}.js* in the subdirectory *javascriptsource{module name}/actions/* of the project directory.

The skeletons of these *.js* files are generated automatically when you save the action, and can the JavaScript actions can immediately be edited in the embedded code editor.

{{% /alert %}}

## 2 Settings

### 2.1 Name

The name of the JavaScript action is used to refer to it from a call to it in a nanoflow. It is also the name of the generated *.js* file.

### 2.2 Parameters

A JavaScript action has zero or more parameters. Parameters are the means by which you pass data into the JavaScript action. In the JavaScript code, you can access the values of the parameters.

Each parameter has a name, type, category, and description. 

Use categories to keep the parameters apart in the [JavaScript Action Call](javascript-action-call). If you do not specify a category, the parameter will appear in the **Input** group.

The types supported by JavaScript actions are described below.

#### 2.2.1 Object

The **Object** parameter type allows the user to pass a Mendix object to the javascript action. you must also select its Entity type, which can be either a specific entity or a type parameter. In the generated JavaScript action template code, this type is represented as a MxObject.

#### 2.2.2 List

The **List** parameter type allows the user to pass a list of Mendix objects to the javascript action you must also select its Entity type, which can be either a specific entity or a type parameter. In the generated JavaScript action template code, this type is represented as an array of MxObject.

#### 2.2.1 Entity Type

The **Entity** parameter type is a placeholder for an entity that will be filled in with the name of the entity when it is called in a nanoflow. Additionally, the entity type can be used to fill in a type parameter. In the generated JavaScript action template code, this type is represented as a string.

#### 2.2.2 Boolean Type 

The **Boolean** parameter type allows users to pass a boolean value to a JavaScript action. 

#### 2.2.3 Date and Time Type

The **Date and time** parameter type allows users of JavaScript actions to pass a date and time value to a JavaScript action. In the generated JavaScript action code the type will be represented as a JavaScript `Date`.

#### 2.2.4 Decimal Type

The **Decimal** parameter type allows users of JavaScript actions to pass a decimal value to a JavaScript action. In the generated JavaScript action code the type will be represented as a [Big](https://www.npmjs.com/package/big-js).

#### 2.2.5 Enumeration Type

The **Enumeration** parameter type allows users of JavaScript actions to pass a enumeration value to a JavaScript action. In the generated JavaScript action code the will be represented as a string.

#### 2.2.6 Integer/Long Type

The **Integer**/**Long** parameter type allows users of JavaScript actions to pass a decimal value to a JavaScript action. In the generated JavaScript action code the type will be represented as a [Big](https://www.npmjs.com/package/big-js).

#### 2.2.7 String Type

The **String** parameter type allows user of JavaScript actions to pass a string value to a JavaScript action.

#### 2.2.8 Return Type

The return type determines the type of the data that the JavaScript action returns. Because many API's are asynchronous you can also return a Promise which resolves to this type. You can use the result of a JavaScriot action in the nanoflowflow in which you call it. ANy type you can use for parameters you can also use as return type.

### 3 Type Parameters

A type parameter is a placeholder for an entity type which will be filled in with a specific entity when it is called in a nanoflow. Type parameters can be used when configuring the data type of a parameter, to allow users to pass an object or a list of an arbitrary entity type.

A JavaScript action has zero or more type parameters. Each type parameter should have a unique name.

### 4 Expose as Nanoflow Action

By selecting the **Expose as nanoflow action** option, it is possible to expose the JavaScript action as a nanoflow action. Exposing the Java action will make it appear in the the **Toolbox** window when editing a nanoflow in the category of your choice. When this action is used in a nanoflow, it will show the provided caption and icon.

The caption and category of the nanoflow action are required, but the icon is optional. When no icon is selected, the default JavaScript action icon is used.

The recommended size for the icon is 16x16.

### 6 Documentation

In the **Documentation** tab of the JavaScript settings tab, you can document the JavaScript action. The documentation is copied into the JavaAScript action as comment on the function in the corresponding *.js* file.

## 3 Code

In the **Code** tab you can edit the JavaScript action code without leaving Studio Pro. The editor is based on the [monaco editor](https://microsoft.github.io/monaco-editor/index.html) which also powers VS Code. It has features like syntax highlighting and code completion.

