### 1.$loacation:返回当前页面的URL
```
 var app=angular.module("myApp",[]);
 app.controller('customersCtrl',function($scope,$location){
     $scope.myUrl = $location.absUrl();
     //获取当前完整的url路径
 })
```
* $location.url();
### 2.$http
### 3.$timeout:延迟
```
var app=angular.module('myApp',[]);

app.controller('myCtrl',function($scope,$timeout){

　　$scope.myHeader="Hello World!";

　　$timeout(function(){

　　　　$scope.myHeader="How are you today?";

　　},2000);
```
### 4.$interval ---对应js的setInterval
```
var app=angular.module('myApp',[]);

app.controller('myCtrl',function($scope,$interval){

　　$scope.theTime=new Date().toLocaleTimeString();

　　$interval(function(){

　　　　$scope.theTime=new Date().toLocaleTimeString();

　　},1000);

});
```
### 5.创建自定义的服务：可以创建访问自定义服务，链接到你的模块中
```
app.service('hexafy',function(){
    this.muFun = function(x){
        return x.toString(16)
    }
})//服务器名字：hexafy
app.controller('myCtrl',function($scope,hexafy){
    $scope.hex = hexafy.myFun(255);
})
```
### 6.在过滤器中使用自定义服务
```
//在过滤器myFormat中使用服务hexafy
app.filter('myFormat',['hexafy',function(hexafy){
    return function(x){
        return hexafy.myFun(x);
    }
}])
```