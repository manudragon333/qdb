# What is angular bootstrapping? Explain process.
* __Bootstrapping__ is the process of initializing, or starting, your Angular app. There are two ways to bootstrap an angular application. - Manual and Auto bootstrapping.
* __Auto bootstrapping__: The _ng-app_ directive is used for auto bootstrapping and indicates the root of the Angular application. Angular reads the HTML within that root and compiles it into an internal representation. This reading and compiling is the bootstrapping process.

Angular initializes / bootstraps automatically upon DOMContentLoaded event or document.readyState is set to complete. At this point AngularJS looks for the ng-app directive, then Angular will:
  * Load the module associated with the directive.
  * Create the application injector.
  * Compile the DOM starting from the ng-app root element.
This process is called auto-bootstrapping.
```
<html>
    <body ng-app="myApp">
        <div ng-controller="Ctrl">Hello {{msg}}!</div>
        <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.5/angular.min.js"></script>
        <script>
            var app = angular.module('myApp', []);
            app.controller('Ctrl', function($scope) {
                $scope.msg = 'Nik';
            });
        </script>
    </body>
</html>
```
* __Manual bootstrapping__  is when we manually initialize angular app by using angular.bootstrap() function instead of using the _ng-app_ directive. This function takes the modules as parameters and should be called within angular.element(document).ready() function.

```
<html>
    <body>
        <div ng-controller="Ctrl">Hello {{msg}}!</div>
        <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.5/angular.min.js"></script>
        <script>
            var app = angular.module('myApp', []);
            app.controller('Ctrl', function($scope) {
                $scope.msg = 'Nik';
            }); 
            //manual bootstrap process 
            angular.element(document).ready(function () { 
              angular.bootstrap(document, ['myApp']); 
            });
        </script>
    </body>
</html>
```
https://stackoverflow.com/questions/21058213/what-is-meant-by-bootstrapping-in-angular-js

# Define dependency injection.

# What is Two-Way binding in Angular JS
Two-way Data binding in AngularJS is maintianing the synchronization between the model and the view.

When data in the model changes, the view reflects the change, and when data in the view changes, the model is updated as well. This happens immediately and automatically, which makes sure that the model and the view is updated/are in sync at all times.

# Explain angular digest cycle.

# When does digest cycle trigger in angular. How to manually trigger a digest cycle?

# 

# $watch() , $digest() and $apply()

# Differences in setTimeout and $timeout
$timeout takes care of the digest cycle. Any changes in setTimeout will need to run the digest cycle manually to reflect in the applciation (Using _$scope.$apply()_ ).

# Services vs Factories vs Providers

# What is isolated scope ? 

# Define custom directives - Full Syntax

# In-Built directives

# Config vs Run

# Routing - Full Syntax

# State Provider

# $http

# $rootScope

# Difference between emit and broadcast

# Ways to communicate between components - Parent to Child, Child to Parent, Sibilings.

# How to change ng- prefix to your custom name

# How to manage dev dependencies
