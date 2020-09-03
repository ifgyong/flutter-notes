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
- [ ] flutter_hooks 
- [x] [3种key的作用 ](https://juejin.im/post/6863300824660082701)


# Google快问快答记录

#### 1. 有没有办法在`widget`放置在应用之前就知晓尺寸？
`LayoutBuilder`的`build`函数可以通过`context`和`constrains`参数让您窒息哦啊将会来放置进来的widget所能使用的空间尺寸，并灵活作出适配。

#### 2. 旋转、倾斜图片和模糊图片的操作需要使用不同的`widget`吗？
这些都是`ImageFilter`的功能，将`imageFilter`类和`BackdropFilter Widget`组合可以使用非常丰富的图片处理效果。

#### 3. 缩略图片放大并成为详情页的头图，这种交互该使用哪个`widget`？

`Hero` widget能方便实现这种转场效果。甚至不局限于图像，通过`Clips`可以做到多样的效果。

#### 4. 如果将需要的动画包含在构造方法中，比较常见的`widget`是什么？

`AnimatedBuilder`，如果仅需要处理不包含额外的状态的用例，使用`AnimatedWidget`即可。

#### 5. 如何让`widget`跟随这数据的变化而更新？

使用`ValueLIstenBuilder` ，其内容和`ValueListenable`保持同步。

#### 6. 如何实现左右滑动删除列表中项目的交互操作？

使用`Dismissable`即可，将这个`widget`朝着`DismissDirection`方向滑动即可移动出视图。

#### 7. 有没有办法不受限于行列布局，而是自由的叠放`widget`？

`stack`可以轻松做到这一点，比较适合自定义一些混合UI，比如将文字跌在图片上等。

#### 8. 有没有更接近底层的方法绘制自定义UI？

可以通过`CustomPaint`做到，里面提供了`canvas`让开发者得以自由的控制每一个笔触和视觉效果。

#### 9.如何在一个`widget`内部实现多种样式文字混排？

`RichText`可以提供完整的富文本功能。除默认意外的文本样式外，里面的每一个`TextSpan`都可以独立设置样式，而实现样式混排。

#### 10. 如何自由调整`ListView`里面项目的顺序？

使用`ReorderableListView`即可让用户自由调整里面的顺序，使用时保证每个子项都有独一无二的`key`。

#### 11. 哪个Widget对 无障碍体验至关重要？

`Semantics`.用它包裹一个`widget`可以让屏幕阅读器，搜索引擎以及其他语义分析工具理解该`widget`的含义。

