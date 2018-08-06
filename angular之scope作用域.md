### 1.scope作用域是应用在（HTML）和js(控制器)之间的纽带
   > scope是一个对象,带有属性和方法；
   当你在AngularJS中创建控制器时，你可以将$scope对象作为一个参数传递；
   ```
   <div ng-app="" ng-controller="myCtrl">
        <h1>{{carname}}</h1>
    </div>

    <script>
        var app=angular.module('myApp',[]);
        app.controller('myCtrl',function($scope){
        $scope.carname="Volvo";           //控制器中创建一个属性名 "carname"，对应了视图中使用 {{ }} 中的名称。
    });
    </script>
   ```
### 2.Scope概述
> angular应用组成：（1）view(视图) （2）model（模型），当前视图中可用的数据； (3)controller（控制器），即js函数，可以添加修改属性
### 3.根作用域 $rootScope
它可以作用在ng-app指令包含的所有HTML元素中
