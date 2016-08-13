# html+css
## 常用的css代码
# git github


# jquery
## 选择器 $()
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

## 方法 ()   ()里是参数
1.属性:
       1)css()   改变样式
       2)index() 获取索引
       3)attr()  改变元素属性
       4)text()  获取文本内容
       5)val()   获取属性内容
2.获取节点:
       1)eq()    通过索引获取元素
       2)siblings  找到同集
       3)parent  找到父集
       4)find    找到子孙集
3.节点操作:
       1)append  在尾部添加节点
       2)prepaend  在顶部添加节点
       3)remove  删除节点(后添加的节点在每绑定事件时无法删除)
       4)before  在同集所添加前添加节点
       5)after   在同集所添加后添加节点
4动画: 
       1)show    显示
       2)hide    隐藏
       3)slideDown 下拉
       4)slideUp 上卷
       5)fadeIn  渐入
       6)fadeOut 渐出
       7)animate 自定义动画
## 事件
1.click 点击事件
  
2.mouseenter  鼠标移入事件
3.mouseleave  鼠标移出事件
4.mousemove   数遍移动事件
5.blur        失去焦点事件

