###layer和layui的区别：

#### layui 是之前 layer laydate 等独立组件的 超集合
#### layui 是一个完整的前端框架，和 Bootstrap 是同一类事务

#### 引入了 layui 之后 layer就不用单独引入了

layui 已经包含了layer

## [再次强调layer只是作为Layui的一个弹层模块，由于其用户基数较大，所以至今仍把她作为独立组件来维护。](http://www.dosrun.com/layui/layui-layer.html)


```
使用场景：
由于layer可以独立使用，也可以通过Layui模块化使用。所以请按照你的实际需求来选择

1、作为独立组件使用layer

引入好layer.js后，直接用即可

<script src="layer.js"></script>
<script>
　　layer.msg('hello'); 
</script>


2、在layui中使用layer

layui.use('layer', function(){
  var layer = layui.layer;
  layer.msg('hello');
});
除了上面有所不同，其它都完全一致。
```

--------------------
### 简单介绍：layer和layui

## [如果你不想使用Layui，而只是想使用layer，你可以去layer独立组件官网下载组件包。你需要在你的页面引入jQuery1.8以上的任意版本，并引入layer.js。](http://www.dosrun.com/layui/layui-layer.html)
## [如果你使用的是Layui，那么你直接在官网下载layui框架即可，无需引入jQuery和layer.js，但需要引入layui.css和layui.js。](http://www.dosrun.com/layui/layui-layer.html)

### layer

### github:[https://github.com/sentsin/layer/](https://github.com/sentsin/layer/)
### 概要

#### layer是一款近年来备受青睐的web弹层组件，这完全得益于她全方位的解决方案。她致力于服务各个水平段的开发人员，您的页面会轻松地拥有丰富友好的操作体验。在与同类组件的比较中，layer总是能轻易获胜。她尽可能地在以更少的代码展现更强健的功能，且格外注重性能的提升、易用和实用性，正因如此，越来越多的开发者将媚眼投上了layer。layer兼容了包括IE6在内的所有主流浏览器。 她数量可观的接口，使得您可以自定义太多您需要的风格，每一种弹层模式各具特色，皆广受欢迎。当然，这种“王婆卖瓜”的陈述听起来总是有点难受，因此你需要进一步了解她是否真的如你所愿。

#### layer致力于打造国内最盛行的弹层组件，为web开发提供强劲动力。

#### 目前layer已经成为国内乃至全世界最多人使用的Web弹层解决方案，并且她仍在与Layui一并高速发展。

#### [官网](http://layer.layui.com/)


-------------------
##layui
### [Layui 简介](http://www.dosrun.com/layui/layui-intro.html)

### github:[https://github.com/sentsin/layui/](https://github.com/sentsin/layui/)

### 经典模块化前端UI框架 

#### Layui 是一款采用自身模块规范编写的国产前端UI框架，遵循原生HTML/CSS/JS的书写与组织形式，门槛极低，拿来即用。其外在极简，却又不失饱满的内在，体积轻盈，组件丰盈，从核心代码到API的每一处细节都经过精心雕琢，非常适合界面的快速开发。layui还很年轻，首个版本发布于2016年金秋，她区别于那些基于MVVM底层的UI框架，却并非逆道而行，而是信奉返璞归真之道，准确地说，她更多是为服务端程序员量身定做，你无需涉足各种前端工具的复杂配置，只需面对浏览器本身，让一切你所需要的元素与交互、从这里信手拈来。

### [官网](http://www.layui.com/)

## 快速上手

获得layui后，将其完整地部署到你的项目目录（或静态资源服务器），你只需要引入下述两个文件：

```
./layui/css/layui.css
./layui/layui.js
```

不用去管其它任何文件。因为他们（比如各模块）都是在最终使用的时候才会自动加载。这是一个基本的入门页面：

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
  <title>开始使用Layui</title>
  <link rel="stylesheet" href="../layui/css/layui.css">
</head>
<body>
 
<!-- 你的HTML代码 -->
 
<script src="../layui/layui.js"></script>
<script>
 
//一般直接写在一个js文件中
layui.use(['layer', 'form'], function(){
  var layer = layui.layer
  ,form = layui.form();
  
  layer.msg('Hello World');
});
</script> 
  
</body>
</html>
```

如果你想快速使用Layui的组件，你还是跟平时一样script标签引入你的js文件，然后在你的js文件中使用layui的组件。但我们更推荐你遵循Layui的模块规范，建立一个自己的模块作为入口：

```
<script>
layui.config({
  base: '/res/js/modules/' //你的模块目录
}).use('index'); //加载入口
</script>    
```

上述的 index 即为你 /res/js/modules/ 目录下的 index.js，它的内容应该如下：

```
/**
  项目JS主入口
  以依赖Layui的layer和form模块为例
**/    
layui.define(['layer', 'form'], function(exports){
  var layer = layui.layer
  ,form = layui.form();
  
  layer.msg('Hello World');
  
  exports('index', {});
});  
```







