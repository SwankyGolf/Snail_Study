## 前端的发展历史

- 1989年

  供职于欧洲粒子物理研究所的Tim Berners Lee（简称李博士）写下了他关于万维网（World Wide Web简称Web）的最初构想

  最初构想：Web作为全球超链接信息共享空间，它是一个抽象的（假想的）信息空间。作为Internet上的一种应用架构。是基于Internet的www+http+url等等技术信息的构想。Web架构

- 1991年

  第一个web页面诞生。早期的功能非常单一：方便看文档、传论文。

  而当年的页面被保存起来，后续一直部署在服务器http://info.cern.ch/hypertext/WWW/TheProject.html

- 1994年——可看做前端历史的起点

  php的出现实现了与数据库的交互以及用于生产动态页面的模板引擎，是Web领域中最主流的服务器语言。动态Web的出现为Web2.0时代奠定了基础。（web1.0全是静态页面，web2.0可以操控后台）

- 1995年

  Javascript这项技术诞生，前端页面不再只是静态的页面交互。我们可以实现前端动态的交互效果。

  1999年：

  微软提出了ajax技术，前端异步请求技术。

  web2.0时代迎来了更好的发展。

- 2007年第一代iphone发布。标志移动互联网的到来。

- 2008年第一台Android发布

- 2014年

  第五代HTML标准发布，HTML5技术

  H5这个版本提出了很多新技术，以前HTML无法实现的内容，H5完全可以实现。

  比如播放视频功能需要借助flash技术，而H5里面直接就内置了视频播放技术。

  平时在开发过程中H5（泛指手机浏览器端）

## 软件开发流程

- 产品经理（了解软件的需求--编写SRS软件需求分析书）

- UI设计师（设计PSD原型图）

- web前端工程师（完美的复原PSD原型图）

- 后端工程师（做项目的功能部分）

- 测试工程师（软件的全面测试）

- 运维工程师（上线）

- 维护

## **PxCook工具的使用**

- PxCook也称之为：**像素大厨**
- 这个工具可以辅助我们前端工程师测量设计稿，确保在开发过程中尺寸的准确性；
- 工具的使用步骤
  - 直接把需要测量的设计稿拖拽到pxcook里面
  - 可以使用快捷键放大和缩小  ctrl  +
  - 移动的快捷键  按住空格键 拖动鼠标即可
  - ctrl+ z  返回上一步

##  processon工具的使用

- 这是一个在线的软件设计工具,每个同学需要自己注册一个账号,可以直接用微信来登录.

- processon地址为:https://www.processon.com/

- 门户网站:比如我们后面要项目实战网页

  地址为:http://web.woniulab.com:8082/

processon工具作用:

1. 可以画流程图
2. 可以设计低保真的原型图(草图)(重点)



## 作业:

使用prosson将这两个页面结构划分出来.

http://web.woniulab.com:8082/index.html

http://web.woniulab.com:8082/paint.html



### WEB前端的核心部分

前端主要由三个核心部分组成：HTML、CSS、JS（JavaScript）。

## 什么是HTML？

官方定义：HTML（Hyper Text Markup Language ）超文本标记语言

超：代表超链接

超文本：指的是通过一系列的超链接，将不同空间里面的资源链接在一起，形成一个网状的可相互连接的结构。可以传递文字、图片、视频、音频等等。浏览器发送一次请求，服务器就可以响应多个资源。

**标记**（也称为标签）：例如**<html></html>**  其中第一个标签是`开始标签`，第二个标签是`结束标签`

<font color="red" size="5">**通俗理解：在记事本当中，用标记写出来的一种计算机标记语言。**</font>

<font color="red" size="5">**注意**</font>：*HTML中所有的标记都是<font color="red">**W3C标准**</font>组织已经规范了，不能自己创建标签。并且每个版本都会有一些差异，HTML有很多版本。目前最新使用最多的版本是H5*

**什么是W3C标准？**

​	万维网联盟（外语缩写：W3C）创建于1994年，是Web技术领域**最具权威和影响力的国际中立性技术标准机构**。到目前为止，W3C已发布了200多项影响深远的Web技术标准及实施指南标准不是某一个标准，而是一系列标准的集合。

### HTML特点：

- 简单性：没有复杂的逻辑，你掌握这些标签的作用，合理搭配就可以设计出网页
- 可扩展：HTML标签有很多功能，新增一个标签就可以带来一个新的功能
- 跨平台：网页的运行环境是浏览器，只要保证你的系统有浏览器就可以运行。
- 通用性：页面写好了之后，可以相互的嵌套。一旦网页设计好了后，任何人都可以访问到你的页面。不管你使用什么浏览器都可以访问。

### HTML文档的结构

```html
<!--代表网页的文档类型，申明了浏览器解析时候的解析规则-->
<!DOCTYPE html>
<html>
	<head>
        <!--强制设置字符集，解决汉字乱码-->
		<meta charset="utf-8">
        <!--声明浏览器渲染方式-->
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
         <!--开启理想视口 如果不写该代码，移动端的默认值则为980px -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <!-- 设置网页的关键字 -->
        <meta name="keywords" content="蜗牛学院">
        <!-- 网页描述 -->
        <meta name="description" content="设置网页的描述">
        <!-- 设置作者 -->
        <meta name="author" content="xiaowoniu">  
		<title>my first page</title>
	</head>
	<body>
		欢迎来到蜗牛学院
	</body>
</html>
```

- html的版本：
      - HTML：1991年，设计出来并没有作为标准。
          - HTML+：1993年，非标准，这个版本已经在W3C的草案中。
          - HTML2.0：1995年发布，这个版本作为了标准。
          - HTML3.2：1997年发布      W3C 推荐标准
          - HTML4.0（HTML4.01）W3C 推荐标准，之前的 PC 端网页规范
          - **HTML5：2012年发布的，新增了很多的新特性。是W3C 推荐标准，它基于移动终端进行了优化**
          - XHTML：存在一段时间，后来就放弃维护，转向H5，既有html规范，又有xml规范

### `<!DOCTYPE html>的作用`:

### 声明网页的文档类型，告诉浏览器解析的规则及html使用版本（目前使用的是H5版本）。

- **注意：必须声明到文档的开头，不区分大小写**

### 常用的 DOCTYPE 声明版本

```html
html5

<!DOCTYPE html>

HTML 4.01 Transitional
该 DTD 包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
HTML 4.01 Frameset
该 DTD 等同于 HTML 4.01 Transitional，但允许框架集内容。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
"http://www.w3.org/TR/html4/frameset.dtd">

XHTML 1.0 Transitional
该 DTD 包含所有 HTML 元素和属性，包括展示性的和弃用的元素（比如 font）。不允许框架集
（Framesets）。必须以格式正确的 XML 来编写标记。 (了解)
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" " http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

### 网页的基本结构

```
<html>
    <head>
        <title>这是标题</title>
    </head>
    <body>
        内容
    </body>
</html>

```

- `<html></html>`:根标签，每个网页有且仅有一个根标签
- `<html></html>`:根标签，每个网页有且仅有一个根标签
- `<head></head>`:代表网页的头部,head主要写CSS代码和js代码。
  - `<title></title>`:代表网页的标题，显示在网页窗口栏，SEO优化有用
  - `<meta charset="utf-8">`:表示网页的编码集，浏览器在解析时会根据这个编码集去解析网页
- `<body></body>`:代表网页的内容区域，主要写网页的结构代码