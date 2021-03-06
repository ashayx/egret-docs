## 概念
DisplayObject类是所有显示对象的父类，该类归纳总结了一些显示对象共有的特性，这些共有的特性被整理成为一些列的属性与方法。

当一个显示对象在舞台中显示的时候，该对象拥有一些非常明显的属性，例如位置，大小等。除此之外显示对象还有一些其他属性，我们来看下图：

![](556533826209f.png)

如上图1所示，在Egret中舞台的坐标系从左上角开始，这是一个非常简单的笛卡尔坐标系。

横轴使用X表示，越向右，X值越大。

纵轴使用Y表示，越向下，Y值越大。

上图1中包含一个灰色的矩形，该矩形拥有一个“锚点”，Egret使用该点的坐标来表示矩形的坐标。当我们使用显示对象创建一个矩形的时候，可以通过 x和y属性来访问修改这个显示对象的坐标位置。示例代码如下：

```
var shape:egret.Shape = new egret.Shape();
shape.x = 100;
shape.y = 20;
```

图2中展示了显示对象的缩放功能。缩放是指将一个显示对象的宽或高进行比例缩放。图中我们对灰色的矩形宽高进行了0.5的缩放，也就是变为原来的50%。缩放功能可以通过 scaleX和scaleY来实现。示例代码如下：

```
var shape:egret.Shape = new egret.Shape();
shape.scaleX = 0.5; 
shape.scaleY = 0.5;
```

> 注意，如果对位图进行缩放或拉伸，图像会发生模糊。

图3中展示了关于alpha透明度的操作。所有显示对象的默认透明度均为"1"，表示完全不透明，我们可以通过 alpha 属性来获取修改透明度。alpha取值范围为 0-1。示例代码如下：

```
var shape:egret.Shape = new egret.Shape();
shape.alpha = 0.4;
```

图4中，展示了显示对象的旋转操作，我们将图中的矩形旋转30°。旋转角度可通过 rotation 属性来访问。示例代码如下：

```
var shape:egret.Shape = new egret.Shape();
shape.rotation = 30;
```

## 可视属性

上面四幅图中中展示了显示对象中比较基础也是很常用的可视属性，下面列表是显示对象的全部可视属性。

* alpha：透明度

* width：宽度

* height：高度

* rotation：旋转角度

* scaleX：横向缩放

* scaleY：纵向缩放

* skewX：横向斜切

* skewY：纵向斜切

* visible：是否可见

* x：X轴坐标值

* y：Y轴坐标值

* anchorOffsetX：对象绝对锚点X

* anchorOffsetY：对象绝对锚点Y

 
