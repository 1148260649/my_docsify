# Docsify 高级使用

## Drawio 绘图软件

### 直接引入

<!-- tabs:start -->

#### **直接引入-效果展示**

[filename](../../img/drawio/test.drawio ':include :type=code')

#### **直接引入-代码示例**

````markdown
[filename](https://cdn.jsdelivr.net/npm/docsify-drawio/test.drawio ':include :type=code')
````

<!-- tabs:end -->

### 导入图片

<!-- tabs:start -->

#### **导入图片-效果展示**

![](../../img/drawio/demo.drawio.png)

#### **导入图片-代码示例**

````markdown
![](demo.drawio.png)
````

<!-- tabs:end -->

## Iframe 使用

### iframe 直接引入

<!-- tabs:start -->

#### **iframe 直接引入-效果展示**

[docsify](../../img/drawio/demo.drawio.png ':include :type=iframe id=a1 width=100% height=400px')

#### **iframe 直接引入-代码示例**

````markdown
[docsify](https://docsify.js.org/#/zh-cn/ ':include :type=iframe id=a1 width=100% height=400px')
````

<!-- tabs:end -->

### iframe 引入mp3

<!-- tabs:start -->

#### **引入mp3-效果展示**

[docsify](../../mp3/徐良-北京巷弄.mp3 ':include :type=audio id=a8 autoplay controls width=100% height=400px')

#### **引入mp3-代码示例**

````markdown
[docsify](../../mp3/徐良-北京巷弄.mp3 ':include :type=audio id=a8 autoplay controls width=100% height=400px')
````

<!-- tabs:end -->

### iframe 引入视频

<!-- tabs:start -->

#### **引入视频-效果展示**

[docsify](../../mp4/test.mp4 ':include :type=video controls width=100% height=520px')

#### **引入视频-代码示例**

````markdown
[docsify](../../mp4/test.mp4 ':include :type=video controls width=100% height=520px')
````

<!-- tabs:end -->

### iframe 导入地图

<!-- tabs:start -->

#### **导入地图-效果展示**

[docsify](https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&layer=mapnik ':include :type=map width=100% height=600px')

#### **导入地图-代码示例**

````markdown
[docsify](https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&layer=mapnik ':include :type=map width=100% height=600px')
````

<!-- tabs:end -->

## 视频示例

<!-- tabs:start -->

#### **视频示例-效果展示**

```html preview
<iframe style="width:800px;min-height:550px;" src="mp4/test.mp4" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

#### **视频示例-代码示例**

````markdown
```html preview
<iframe style="width:800px;min-height:550px;" src="mp4/test.mp4" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```
````

<!-- tabs:end -->