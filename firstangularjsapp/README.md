# Chapter 2 - Your First Angular App

### How to modify simple HTML Page to use AngularJS?
1. Add angular.js sources:

```html
<script src="../angular-1.3.14/angular.js"></script>
```

2. Create AngularJS module and add ng-app to <html> or <body> element:

**angular.module(...)** function is passed 2 or more arguments

```html
angular.module(name, [requires], [configFn]);
```
 * **name** (String) - name of the module to create or retrieve
 * **requires** (optional, Array[String]) - If specified then new module being created, if unspecified new module is being retrieved for further configuration
 * **configFn** (optional, Function) - optional configuration function

```html
<script>
    var todoApp = angular.module("todoApp", []);
</script>
```

**ng-app** attribute places within HTML element, tells browser that particular HTML tag contains elements (children) that should be compiled before usage and processed by AngularJS

```html
<html ng-app="todoApp">
```

# Sources
 * Freeman Adam, Pro AngularJS (pages 15-45, http://www.apress.com/9781430264484?gtmf=b)
 * AngularJS Developer Guider, Module (https://docs.angularjs.org/guide/module)
 * AngularJS API, Module Function (https://docs.angularjs.org/api/ng/function/angular.module)