# Chapter 2 - Your First Angular App

### How to modify simple HTML Page to use AngularJS?

##### Add angular.js sources:

    ```html
    <script src="../angular-1.3.14/angular.js"></script>
    ```

##### Create AngularJS module and add ng-app to <html> or <body> element:

**angular.module(...)** function is passed 2 or more arguments

    ```html
    angular.module(name, [requires], [configFn]);
    ```
 * **name** (String) - name of the module to create or retrieve
 * **requires** (optional, Array[String]) - If specified then new module being created, if unspecified new module is being retrieved for further configuration
 * **configFn** (optional, Function) - optional configuration function

    ```html
    <script>
        var appModuleVar = angular.module("appModuleVar", []);
    </script>
    ```

**ng-app** attribute places within HTML element, tells browser that particular HTML tag contains elements (children) that should be compiled before usage and processed by AngularJS

    ```html
    <html ng-app="appModuleVar">
    ```

#### MVC Introduction
 * Breaks application into 3 separate areas: model, view, controller
 * Model - data of the application
 * Controller - logic/behavior performing operations on data
 * View - displays data
 
##### Model Introduction
 * Main purpose: Separates the data from HTML elements
 * Uses JSON notation
 
##### Controller Introduction
 * Connector between the data and the view (supplies view with data hold by the model)
 * Avoidance of direct view-model access
 
##### View Introduction
 * HTML page

#### How AngularJS enables MVC usage?

##### Controller within AngularJS
Basic information:
 * $scope - variable that provides initial state of a scope, properties of $scope variable can be accessed from view (exposes data to views)
 * $ - refers to build-in service, which is self-contained component that provides features to multiple controllers
 
Usage:

1. Create controller by **module.controller(...)** function method invocation:

    ```html
    <script>
        todoApp.controller("ContollerName", function ($scope) {
            $scope.variable = model;
        });
    </script>
    ```

2. Specify the HTML element (region) where controller will be used (**ng-controller** attribute):

    ```html
    <body ng-controller="ContollerName">
    ```

##### View within AngularJS
1. Add elements to $scope (Controller within AngularJS).
2. **Data Binding** - {{...}}
 * Context of Data Binding is evaluated as JS expression
 * You can access elements that are assigned to $scope variable of used controller ($scope.<variableName>)
 
    ```html
    <div class="page-header">
        <h1>
            {{variable.property}}
        </h1>
    </div>
    ```

 * **ng-model** attribute - simple property access
    ```html
    <input ... ng-model="variable.property" />
    ```

 * **ng-repeat** attribute - for array element enumeration
    ```html
    <tr ng-repeat="loopVar in someModelArray">
        <td>{{loopVar.property}}</td>
    </tr>
    ```

3. 

# Sources
 * Freeman Adam, Pro AngularJS (pages 15-45, http://www.apress.com/9781430264484?gtmf=b)
 * AngularJS Developer Guider, Module (https://docs.angularjs.org/guide/module)
 * AngularJS API, Module Function (https://docs.angularjs.org/api/ng/function/angular.module)
 * AngularJS Developer Guide, Controllers (https://docs.angularjs.org/guide/controller)
 * AngularJS API, ng-controller (https://docs.angularjs.org/api/ng/directive/ngController)
