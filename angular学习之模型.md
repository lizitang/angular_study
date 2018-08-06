### 1.ng-bind  
  > 内容放到标签的innerHTML中
### 2.ng-model
  > 为应用程序数据提供类型验证（number、email、required（input属性，必填字段））。为应用程序数据提供状态（invalid、dirty、touched、error）。
  ```
	<div ng-app="myApp" ng-controller="myCtrl">

　　		名字：<input ng-model="name">

	</div>

	<script>

		var app=angular.module("myApp",[]);
		app.controller("myCtrl",function($scope){
			$scope.name="John Doe";
		})

	});
        </script>
   ```
#### 验证用户输入：$error
```
	<form ng-app="" name="myForm">

　　      Email:

　　	  <input type="email" name="myAddress" ng-model="text">

　　	  <span ng-show="myForm.myAddress.$error.email">不是一个合法的邮箱地址</span>

	</form>
```

> 应用状态：ng-model指令可以为应用数据提供状态值(invalid,dirty,touched,error):

        Valid: true (如果输入的值是合法的则为 true)。

        Dirty: false (如果值改变则为 true)。

        Touched: false (如果通过触屏点击则为 true)。
> css 类：ng-model指令基于它们的状态为HTML元素提供了CSS类
```
<style>

input.ng-invalid{

　　background-color:lightblue;

};

</style>

<body>

<form ng-app="" name="myForm">

　　输入你的名字：

　　<input name="myaddress" ng-model="text" required>

</form>

</body>
```

### 3.ng-init 初始化数据（不经常用）
### 4.angular的指令
	
	ng-repeat 循环（用在一个对象数组上）
### 5.创建自定义指令：
	.directive函数来添加自定义指令