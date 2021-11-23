###  针对angularJS的学习用于thingsboard2.5的前端组件的开发
#### 什么是angularJS
扩展HTML，将数据绑定到HTML元素上  
操作HTMl元素  
在HTml背后添加代码  
通过ng-app创建一个angular应用，通过model将数据绑定到应用，通过ng-bind将应用数据绑定到HTML  
angularJS表达式，看起来有点像jsp的<%表达式作用也很像，用于存放表达式  
### 表达式
{{}} 效果与<span ng-bind = ></span>相近  
#### 能操作的对象
+ 数字
+ 字符串
+ 对象
+ 数组  
### 指令
带有ng-前缀  
+ ##### 数据绑定
    通过ng-model  
+ ##### 重复
    通过ng-repeat，遍历
```
    
<div ng-app="" ng-init="names=['Jani','Hege','Kai']">
  <p>使用 ng-repeat 来循环数组</p>
  <ul>
    <li ng-repeat="x in names">
      {{ x }}
    </li>
  </ul>
</div>
```
+ ##### 创建自定义指令
    app.derictive("函数名",function(){})；创建。注意的是在生命的时候要用驼峰命名法，而在使用时要使用-分割驼峰。使用restrict来限制使用情景
```
  <script>
  var app = angular.module("myApp", []);
  app.directive("runoobDirective", function() {
      return {
          template : "<h1>自定义指令!</h1>"
      };
  });
  </script>
```

