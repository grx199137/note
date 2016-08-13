# html+css
## 常用的css代码
# git github


# jquery
## 一.选择器 $()
   引用jquery.js文件
   例:
   ```html 
   <body>
   <div class="box"></div>
   <script src="script/jquery.js"></script> 
   <script>
       $(".box")
   </script>   
   </body>
   ```
## 二.方法 ()   ()里是参数
###1.属性:
       1)css()   改变样式
       2)index() 获取索引
       3)attr()  改变元素属性
       4)text()  获取文本内容
       5)val()   获取属性内容
###2.获取节点:
       1)eq()    通过索引获取元素
       2)siblings  找到同集
       3)parent  找到父集
       4)find    找到子孙集
###3.节点操作:
       1)append  在尾部添加节点
       2)prepaend  在顶部添加节点
       3)remove  删除节点(后添加的节点在每绑定事件时无法删除)
       4)before  在同集所添加前添加节点
       5)after   在同集所添加后添加节点
###4动画: 
       1)show    显示
       2)hide    隐藏
       3)slideDown 下拉
       4)slideUp 上卷
       5)fadeIn  渐入
       6)fadeOut 渐出
       7)animate 自定义动画
## 三.事件
###1.click 点击事件
  7-11例1）点击变换图片属性
  思路:点击事件获取li的索引,然后通过索引重新设置images的路径
  ```html
  <body>
    <img src="" alt="" id="pic">
    <ul id="num-list">
      <li>1</li>
      <li>2</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
    </ul>
    <script src="script/jquery.js"></script>
    <script>
    $("num-list li").click(function(){
      var index = $(this).index();
      var src = "images/" + index + ".jpg";
      $("#pic").attr("src",src);
    })
    </script>
  </body>
  ```
###2.mouseenter  鼠标移入事件
  7-12例1) 下拉菜单
  思路:鼠标移入ul时菜单下拉，移除时上卷的动画效果
  ```html
  <body>
  <ul id="nav">
    <li>
      服装
      <ul class="list">
        <li>裤子</li>
        <li>衣服</li>
        <li>裙子</li>
      </ul>
    </li>
    <li>
      <a href="">价格</a>
      <ul class="list">
        <li>100</li>
        <li>200</li>
        <li>500</li>
      </ul>
    </li>
    <li>
      <a href="">品牌</a>
      <ul class="list">
        <li>骆驼</li>
        <li>李宁</li>
        <li>阿玛尼</li>
      </ul>
    </li>
  </ul>
  <script src="script/jquery.js"></script>
  <script>
      $("#nav>li").mouseenter(function(){
        $(this).find("li").stop().slideDown(500);
      }).mouseleave(function(){
        $(this).find("li").stop().slideUp(500);
      })
  </script>
  </body>
  ```
###3.mouseleave  鼠标移出事件
###4.mousemove   数遍移动事件
###5.blur        失去焦点事件
# javascript
# node
## 一.关于node
### 1.node的含义
  node就是通过js实现把html界面与数据分离的技术
### 2.node的模块
    1)自定义模块
    2)核心模块
    3)第三方模块
### 3.第三方模块创建服务器
    8-11例1) 创建服务器
    思路:首先用下载好的node软件,命令行npm install express下载第三方模块,用核心模块自带的path方法创建静态的网页通过服务器来显示
    ```html
    var express = require("express");
    var app = express();
    var path = require("path");
    app.use(express.static(path.join(__dirname,"public")));
    app.listen(3000,function(){
    console.log("服务器已经开启");
    })
    ```

