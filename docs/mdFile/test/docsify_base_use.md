# docsify 插件用法

## 提示信息

> 依赖插件： [docsify-plugin-flexible-alerts](https://www.npmjs.com/package/docsify-plugin-flexible-alerts)

### 代码示例

```markdown
> [!TIP]
> 这是一个提示

> [!NOTE]
> 这是一个记录

> [!WARNING]
> 这是一个警告

> [!ATTENTION]
> 这是一个错误
```

### 效果展示
>
> [!TIP]
> 这是一个提示

> [!NOTE]
> 这是一个记录

> [!WARNING]
> 这是一个警告

> [!ATTENTION]
> 这是一个错误

---

## 问答展示（手风琴）

> 依赖插件： [docsify-accordion](https://www.npmjs.com/package/docsify-accordion)
>
### 代码示例

```markdown
+ 问题1? +

    [制表符]答案1

+ 问题2? +

    答案2  
    [制表符]第二行

+ 问题1 +

    [制表符]回答1  

+ 问题3 +

    [制表符]回答3
```

### 效果展示

+ 问题1? +

    答案1

+ 问题2? +

    答案2  
    第二行

+ 问题1 +

    回答1  

+ 问题3 +

    回答3

---

## tab（标签页）

> 依赖插件： [docsify-tabs](https://www.npmjs.com/package/docsify-tabs)

### 代码示例

```markdown
<!-- tabs:start -->

#### **Bold**

内容：**Bold**

#### **`<em>`Italic`</em>`**

内容：**`<em>`Italic`</em>`**

#### **`<span style="color: red;">`Red**

内容：**`<span style="color: red;">`Red**

#### **😄**

内容：**😄**

#### **😀**

内容：**😀**

#### **Badge `<span class="tab-badge">`New!**

内容：**Badge `<span class="tab-badge">`New!**

<!-- tabs:end -->

```

### 效果展示

<!-- tabs:start -->

#### **Bold**

内容：**Bold**

#### **`<em>`Italic`</em>`**

内容：**`<em>`Italic`</em>`**

#### **`<span style="color: red;">`Red**

内容：**`<span style="color: red;">`Red**

#### **😄**

内容：**😄**

#### **😀**

内容：**😀**

#### **Badge `<span class="tab-badge">`New!**

内容：**Badge `<span class="tab-badge">`New!**

<!-- tabs:end -->

---

## HTML 预览示例

> 官网：[docsify-demo](https://www.npmjs.com/package/docsify-demo)

### 代码示例

````html
```html preview
<p>Hello, World.</p>
```
````

### 效果展示

```html preview
  <p>Hello Docsify</p>
<b style="color: red;">Inline styles are supported too.</b>
<b style="color: blue;">Test.</b>
<div>
    <span>
        <b style="color: blue;">Test.</b>
    </span>
</div>
```

---

## 加载远程md文件

### 代码示例

````markdown
[rmd](远程md文档路径地址)
```
````

### 效果展示

---

## 分栏

> 官网：[docsify-demo](https://www.npmjs.com/package/docsify-pdf-embed-plugin)

### 代码示例

```markdown
<!-- panels:start -->
<!-- div:title-panel -->

  (...) - Awesome title

<!-- div:left-panel -->

  (...) - Awesome explanation

<!-- div:right-panel -->

  (...) - Awesome example

<!-- panels:end -->
```

### 效果展示
<!-- panels:start -->
<!-- div:title-panel -->

  (...) - Awesome title

<!-- div:left-panel -->

  (...) - Awesome explanation

<!-- div:right-panel -->

  (...) - Awesome example

<!-- panels:end -->

---

## pdf预览

> 官网：[docsify-pdf-embed-plugin](https://www.npmjs.com/package/docsify-pdf-embed-plugin)

### 代码示例

````txt
```pdf
[文件路径]
```
````

### 效果展示

```pdf
../../pdf/优知学院-Spring Boot面试题与答案.pdf
```

---

## PlantUml 图绘制

> 官网： <https://plantuml.com/zh/>

> [!ATTENTION]
> 该功能需要联网

### 序列图

#### 代码示例

````markdown
```plantuml
@startuml
Alice -> Bob: Authentication Request
Bob --> Alice: Authentication Response

Alice -> Bob: Another authentication Request
Alice <-- Bob: Another authentication Response
@enduml
```
````

#### 效果展示

![](../../img/plantUml/序列图.svg)

### 声明参与者

```plantuml
@startuml
participant Participant as Foo
actor       Actor       as Foo1
boundary    Boundary    as Foo2
control     Control     as Foo3
entity      Entity      as Foo4
database    Database    as Foo5
collections Collections as Foo6
queue       Queue       as Foo7
Foo -> Foo1 : To actor
Foo -> Foo2 : To boundary
Foo -> Foo3 : To control
Foo -> Foo4 : To entity
Foo -> Foo5 : To database
Foo -> Foo6 : To collections
Foo -> Foo7: To queue
@enduml

```

#### 代码示例

````markdown

```plantuml
@startuml
actor Bob #red
' The only difference between actor
'and participant is the drawing
participant Alice
participant "I have a really\nlong name" as L #99FF99
/' You can also declare:
   participant L as "I have a really\nlong name"  #99FF99
  '/

Alice->Bob: Authentication Request
Bob->Alice: Authentication Response
Bob->L: Log transaction
@enduml
```
````

#### 效果展示

![](../../img/plantUml/参与者2.svg)

### json 图

#### 代码示例

````markdown
```plantuml
@startjson
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 27,
  "address": {
    "streetAddress": "21 2nd Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10021-3100"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "212 555-1234"
    },
    {
      "type": "office",
      "number": "646 555-4567"
    }
  ],
  "children": [],
  "spouse": null
}
@endjson
```
````

#### 效果展示

![](../../img/plantUml/json.svg)

### 类图

```plantuml
@startuml
abstract        abstract
abstract class  "abstract class"
annotation      annotation
circle          circle
()              circle_short_form
class           class
class           class_stereo  <<stereotype>>
diamond         diamond
<>              diamond_short_form
entity          entity
enum            enum
exception       exception
interface       interface
metaclass       metaclass
protocol        protocol
stereotype      stereotype
struct          struct
@enduml

```

### 思维导图

#### 代码示例

````markdown
```plantuml
@startmindmap
+[#Orange] Colors
++[#lightgreen] Green
++[#FFBBCC] Rose
--[#lightblue] Blue
@endmindmap

```

````

#### 效果展示

![](../../img/plantUml/思维导图.svg)
