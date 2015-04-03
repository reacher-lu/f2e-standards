淘维 web 前端开发规范-XHTML规范
=====================
*美店等项目前端规范*


## <a name='TOC'>目录</a>

  1. [文档声明](#doctype)
  1. [W3C标准](#w3c)
  1. [标签语义化](#semantic)
  1. [其他](#others)
  1. [原则](#rules)



## <a name='doctype'>文档声明</a>

- 文档类型声明及编码: 统一为html5声明类型<!DOCTYPE html>; 编码统一为\<meta charset="utf-8" /\>
  ```html
  
  <!DOCTYPE html>
  <html>
  <head>
    <meta charset="utf-8" />
    <title>{{title}}</title>
    <meta name="keywords" content="{{keywords}}" />
    <meta name="description" content="{{description}}" />
    
  ```
- 书写时利用IDE实现层次分明的缩进，缩进使用2个空格;



## <a name='w3c'>[W3C](http://www.w3.org/)标准</a>

- 所有标签都必须闭合，如果是单独不成对的标签，在标签最后加一个"/"来关闭它，如 br (\<br /\>), hr($\<hr /\>)等;

- 所有的属性必须用引号""括起来，不要不加，也不要使用单引号（如 name="Reacher's dog"）&quot; &apos;

- 标签禁止使用大写字母，所有标签的元素和属性的名字都必须小写

- 把所有<和&等特殊符号用编码表示

  + 任何小于号（<），不是标签的一部分，都必须被编码为&lt;
  + 任何大于号（>），不是标签的一部分，都必须被编码为&gt;
  + 任何与号（&），不是实体的一部分的，都必须被编码为&amp;




## <a name='semantic'>标签语义化</a>

- 使用有语义的标签（如标题使用h1-h5标签，段落使用p标签，列表使用ul,ol等）（理论上一个页面只出现一次h1）

- 使用html5新标签（section,article,figure,figcaption,header,nav,aside等）

- 严禁在行内元素内嵌套块级元素

- 对于图片及背景图片，需考量它的语义，如果是作为icon及背景存在，则需作为背景图片




## <a name='others'>其他</a>

- 链接地址尽量必须避免重定向，如：href="http://meidian.com/", 需在URL后面加上/；

- 考虑到结构与表现的分离，在页面中尽量避免使用style属性,即style="…";

- 给区块代码及重要功能(比如循环)加上注释, 方便后台添加功能

- 模块化开发中少使用ID（可以动态赋ID），可使用data-属性，便于复用




## <a name='rules'>原则</a>

- 不要为了解决样式问题而去增加毫无意义的标签

- 保证页面的[可访问性](http://www.douban.com/group/topic/5135474/)，理论上当去掉所有的javascript，css，页面依旧可读





