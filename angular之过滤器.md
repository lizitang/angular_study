### 1.过滤器可以使用一个管道字符（|）添加到表达式和指令中；
### 2.angularjs过滤器可用于转换数据：
* currency:格式化数字为货币格式；
* filter:从数组项中选择一个子集；
* lowercase：小写
* uppercase: 大写、
* orderBy:根据某个表达式排序数组
```
<div ng-app="myApp" ng-controller="namesCtrl">

<p><input type="text" ng-model="test"></p>

<ul>

　　<li ng-repeat="x in name | filter:test | orderBy:'country'">

　　　　{{(x.name | uppercase) +',' +x.country}}

　　</li>

</ul>

</div>
```
