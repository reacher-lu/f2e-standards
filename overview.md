淘维 web 前端开发规范-概述
=====================
*美店等项目前端规范*


## <a name='TOC'>目录</a>

  1. [规范列表](#list)
  1. [项目结构](#folder)
  1. [样式书写](#class)
  1. [资源加载](#load)



## <a name='list'>规范列表</a>

  + `[页面规范](./html.md)（html）`
  + `[样式规范](./css.md)（css）`
  + `[脚本规范](./javascript.md)（javascript）`
  + `[移动web开发规范](./mobile.md)`



## <a name='folder'>项目结构</a>

- css文件统一放置在命名为styles的文件夹下，脚本文件统一放置在命名为scripts的文件夹下，图片文件统一放置在命名为images的文件夹下
- styles文件夹应至少包含以下目录
  + global      全局样式，特指所有项目都通用的样式，包括reset，sass公用的方法等
  + common      本项目共用样式，包括页头，页脚，UI的全局规范，sass主函数等
  + components  组件的样式，UI组件规范的样式（如buttons集等等）
  + shim        外部引用的一些css
  + dev         开发目录
  + fonts       用于放置字体文件

- images文件夹应至少包含以下目录,img图片名称，多个单词之间以_分隔
  + icon   用于放置图标文件
  + test   用于放置测试图片

- scripts文件夹包含的目录以具体前端架构为准

- PSD 所有收到的PSD文件，页面布局中产生的spritesPSD都须按照项目分门别类




## <a name='class'>样式书写</a>

- 所有样式定义 在class中，id与data-xxx 只用于js操作
- 页面中如非必要，不要使用style=""属性，也不要使用诸如：
    + \<style\>…\</style\>
    + \<script src="…"\>\</script\>

  等页面内的样式及脚本


## <a name='load'>资源加载</a>

- css样式表统一放到head里面，js文件统一放到页面底部，
- 使用grunt，gulp等构建工具压缩，合并静态文件，尽可能少的减少图片请求



