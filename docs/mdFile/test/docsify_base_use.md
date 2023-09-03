# docsify 插件用法

<!-- panels:start -->
<!-- div:title-panel -->

## 提示信息

> 依赖插件： [docsify-plugin-flexible-alerts](https://www.npmjs.com/package/docsify-plugin-flexible-alerts)

<!-- div:left-panel -->

**效果展示**

> [!TIP]
> 这是一个提示

> [!NOTE]
> 这是一个记录

> [!WARNING]
> 这是一个警告

> [!ATTENTION]
> 这是一个错误

<!-- div:right-panel -->

**代码示例**

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

<!-- panels:end -->

---

<!-- panels:start -->
<!-- div:title-panel -->

## 问答展示（手风琴）

> 依赖插件： [docsify-accordion](https://www.npmjs.com/package/docsify-accordion)

<!-- div:left-panel -->

**效果展示**

+ 问题1? +

    答案1

+ 问题2? +

    答案2  
    第二行

+ 问题1 +

    回答1  

+ 问题3 +

    回答3

<!-- div:right-panel -->

**代码示例**

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

<!-- panels:end -->

---

<!-- panels:start -->
<!-- div:title-panel -->

## tab（标签页）

> 依赖插件： [docsify-tabs](https://www.npmjs.com/package/docsify-tabs)

<!-- div:left-panel -->

**效果展示**

<!-- tabs:start -->

#### **Bold**

内容：**Bold**

#### **<em>Italic</em>**

内容：**<em>Italic</em>**

#### **<span style="color: red;">Red**

内容：**<span style="color: red;">Red**

#### **😄**

内容：**😄**

#### **😀**

内容：**😀**

#### **Badge <span class="tab-badge">New!**

内容：**Badge <span class="tab-badge">New!**

<!-- tabs:end -->

<!-- div:right-panel -->

**代码示例**

```markdown
<!-- tabs:start -->

#### **Bold**

内容：**Bold**

#### **<em>Italic</em>**

内容：**<em>Italic</em>**

#### **<span style="color: red;">Red**

内容：**<span style="color: red;">Red**

#### **😄**

内容：**😄**

#### **😀**

内容：**😀**

#### **Badge <span class="tab-badge">New!**

内容：**Badge <span class="tab-badge">New!**

<!-- tabs:end -->

```

<!-- panels:end -->

---

<!-- panels:start -->
<!-- div:title-panel -->

## HTML 预览示例

> 官网：[docsify-demo](https://www.npmjs.com/package/docsify-demo)

<!-- div:left-panel -->

**效果展示**

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
<!-- div:right-panel -->

**代码示例**

````html
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
````

<!-- panels:end -->

---

## 加载远程md文件

<!-- tabs:start -->

#### **加载远程md文件效果展示**

#### **加载远程md文件代码示例**

````markdown
[rmd](远程md文档路径地址)
````

<!-- tabs:end -->
---

## 分栏

> 官网：[docsify-example-panels](https://www.npmjs.com/package/docsify-example-panels)

<!-- tabs:start -->

#### **分栏效果展示**

<!-- panels:start -->
<!-- div:title-panel -->

  (...) - Awesome title

<!-- div:left-panel -->

  (...) - Awesome explanation

<!-- div:right-panel -->

  (...) - Awesome example

<!-- panels:end -->
#### **分栏代码示例**

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

<!-- tabs:end -->

---

## pdf预览

> 官网：[docsify-pdf-embed-plugin](https://www.npmjs.com/package/docsify-pdf-embed-plugin)

<!-- tabs:start -->

### **效果展示**

```pdf
pdf/优知学院-Spring Boot面试题与答案.pdf
```

### **代码示例**

````txt
```pdf
[文件路径]
```
````

<!-- tabs:end -->

---

## 网站计数

> 官网：[docsify-busuanzi](https://www.npmjs.com/package/docsify-busuanzi)

---

## PlantUml 图绘制

> 官网： <https://plantuml.com/zh/>

> [!ATTENTION]
> 该功能需要联网

<!-- panels:start -->
<!-- div:title-panel -->

### 序列图

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/序列图.svg)

<!-- div:right-panel -->

**代码示例**

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

<!-- panels:end -->

***

<!-- panels:start -->
<!-- div:title-panel -->

### 声明参与者

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/参与者2.svg)

<!-- div:right-panel -->

**代码示例**

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

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/声明参与者2.svg)

<!-- div:right-panel -->

**代码示例**

````markdown
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
````

<!-- panels:end -->

***

<!-- panels:start -->
<!-- div:title-panel -->

### json 图

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/json.svg)

<!-- div:right-panel -->

**代码示例**

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

<!-- panels:end -->

***

<!-- panels:start -->
<!-- div:title-panel -->

### 类图

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/类图.svg)

<!-- div:right-panel -->

**代码示例**

````markdown
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

````

<!-- panels:end -->

***

<!-- panels:start -->
<!-- div:title-panel -->

### 思维导图

<!-- div:left-panel -->

**效果展示**

![](../../img/plantUml/思维导图.svg)

<!-- div:right-panel -->

**代码示例**

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

<!-- panels:end -->

<!-- tabs:start -->

#### **效果展示**

```plantuml
@startmindmap
* Java基础
** Java发展历史
** 安装Java环境
** Hello World
**[#yellow] 基本语法
*** 变量
*** 数据类型
**** 基本数据类型
*****_ boolean
*****_ byte
*****_ short
*****_ char
*****_ int
*****_ long
*****_ float
*****_ double
**** 引用数据类型
*****_ class类
*****_ array[]数组
*****_ interface接口
**** 运算符
*****_ 四则运算符
*****_ 增量运算符
*****_ 四则运算符
*****_ 自增与自减运算符
*****_ 关系运算符
*****_ 逻辑运算符
*****_ 位运算符
*****_ 移位运算符
*****_ 三目运算符
*****_ 优先级
**** 循环
**** 条件和多分支
**** Java关键字
--[#green] 面向对象
--- 类和对象
--- 继承
--- 重载
--- 重写
--- 多态
--[#pink] 高级特性
--- 接口
--- 泛型
--- 异常处理
--- 注解
--- 反射
@endmindmap
```

#### **代码示例**

````markdown
```plantuml
@startmindmap
* Java基础
** Java发展历史
** 安装Java环境
** Hello World
**[#yellow] 基本语法
*** 变量
*** 数据类型
**** 基本数据类型
*****_ boolean
*****_ byte
*****_ short
*****_ char
*****_ int
*****_ long
*****_ float
*****_ double
**** 引用数据类型
*****_ class类
*****_ array[]数组
*****_ interface接口
**** 运算符
*****_ 四则运算符
*****_ 增量运算符
*****_ 四则运算符
*****_ 自增与自减运算符
*****_ 关系运算符
*****_ 逻辑运算符
*****_ 位运算符
*****_ 移位运算符
*****_ 三目运算符
*****_ 优先级
**** 循环
**** 条件和多分支
**** Java关键字
--[#green] 面向对象
--- 类和对象
--- 继承
--- 重载
--- 重写
--- 多态
--[#pink] 高级特性
--- 接口
--- 泛型
--- 异常处理
--- 注解
--- 反射
@endmindmap
```
````

<!-- tabs:end -->
