# flutter-notes
记录一下学习的问题和答案


## 清单
 
- [x] [渲染原理](https://juejin.im/post/6865554947941859335)/局部刷新/优化帧数
- [x] [异步/多线程](https://juejin.im/post/5f1fe4906fb9a07e6d70d8a0)
- [x] [flutter_bloc](https://juejin.im/post/6862932168729952264) /[redux](https://juejin.im/post/6860747643493515278)/[Provider](https://juejin.im/post/6862150535043252237)/[ScopedModel](https://juejin.im/post/6860001014289416205) 原理
- [ ] dio/HttpClick
- [ ] animations 动画
- [ ] flutter_spinkit
- [ ] animated_text_kit 2.2.0
- [ ] simple_animations
- [ ] rxdart
- [ ] image_cropper 编辑图片
- [x] [3种key的作用 ](https://juejin.im/post/6863300824660082701)
- [ ] map linkmap 区别
- [ ] 线程模型
- [ ] vm虚拟机
- [ ] 布局流程、绘制流程、触摸事件分发流程、gs回收算法、iOS引用循环、内存抖动、内存溢出、Error  和Exception区别、Imk机制，runloop、全局变量和局部变量在堆栈问题、block原理、加密算法、图片加载优化、缓存原理、



## iOS 
- [1. 多线程考察题目和答案](./1.多线程题目.md)
- [2. iOS 渲染原理解析 2020.5.27 冬瓜公众号](https://mp.weixin.qq.com/s/6ckRnyAALbCsXfZu56kTDw) [/离屏渲染触发条件和避免手段](./2.离屏渲染.md)
- [3. iOS Memory 内存详解 2020.6.29 冬瓜公众号](https://mp.weixin.qq.com/s?__biz=MzA5MTM1NTc2Ng==&mid=2458322852&idx=1&sn=b3be904d955b20e292e3c2683e2b64f0&chksm=870e08bdb07981abdc9a847b6db5135ac58f651f3eda02b09e1120b7df402d8e5afa94b08eea&scene=178#rd)
- [4. 内存释放优化](https://elliotsomething.github.io/2017/05/21/%E5%86%85%E5%AD%98%E9%87%8A%E6%94%BE%E4%BC%98%E5%8C%96/)/[子线程渲染](https://www.jianshu.com/p/dbada5f44ac1)
- [5. ]()

# iOS面试题 2020.10.28
## 多线程面试题
## Block面试题
## 网络编程面试题
## 设计模式面试题
## 常用算法面试题
## 数据结构面试题
## 内存管理面试题
## 数据库面试题
## CPU和启动优化面试题
## Runtime运行时面试题
## 事件处理机制面试题
## Runloop面试题
## 渲染机制面试题
## UI相关面试题
## 无痕埋点
### [无痕埋点](无痕埋点.md)
## 卡顿监测
### [卡顿监测](监测卡顿方案.md)

# Google快问快答记录

### 1. 有没有办法在`widget`放置在应用之前就知晓尺寸？
`LayoutBuilder`的`build`函数可以通过`context`和`constrains`参数让您窒息哦啊将会来放置进来的widget所能使用的空间尺寸，并灵活作出适配。

### 2. 旋转、倾斜图片和模糊图片的操作需要使用不同的`widget`吗？
这些都是`ImageFilter`的功能，将`imageFilter`类和`BackdropFilter Widget`组合可以使用非常丰富的图片处理效果。

### 3. 缩略图片放大并成为详情页的头图，这种交互该使用哪个`widget`？

`Hero widget`能方便实现这种转场效果。甚至不局限于图像，通过`Clips`可以做到多样的效果。

### 4. 如果将需要的动画包含在构造方法中，比较常见的`widget`是什么？

`AnimatedBuilder`，如果仅需要处理不包含额外的状态的用例，使用`AnimatedWidget`即可。

### 5. 如何让`widget`跟随这数据的变化而更新？

使用`ValueListenBuilder` ，其内容和`ValueListenable`保持同步。

### 6. 如何实现左右滑动删除列表中项目的交互操作？

使用`Dismissable`即可，将这个`widget`朝着`DismissDirection`方向滑动即可移动出视图。

### 7. 有没有办法不受限于行列布局，而是自由的叠放`widget`？

`stack`可以轻松做到这一点，比较适合自定义一些混合`UI`，比如将文字跌在图片上等。

### 8. 有没有更接近底层的方法绘制自定义UI？

可以通过`CustomPaint`做到，里面提供了`canvas`让开发者得以自由的控制每一个笔触和视觉效果。

### 9.如何在一个`widget`内部实现多种样式文字混排？

`RichText`可以提供完整的富文本功能。除默认意外的文本样式外，里面的每一个`TextSpan`都可以独立设置样式，而实现样式混排。

### 10. 如何自由调整`ListView`里面项目的顺序？

使用`ReorderableListView`即可让用户自由调整里面的顺序，使用时保证每个子项都有独一无二的`key`。

### 11. 哪个Widget对 无障碍体验至关重要？

`Semantics`.用它包裹一个`widget`可以让屏幕阅读器，搜索引擎以及其他语义分析工具理解该`widget`的含义。

