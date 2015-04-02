淘维 web 前端开发规范-CSS规范
=====================
*美店等项目前端规范*


## <a name='TOC'>目录</a>

  1. [准备工作](#prepare)
  1. [顺序与格式](#format)




## <a name='prepare'>准备工作</a>

- 书写代码前, 考虑并提高样式重复使用率;

- 尽量不要直接给标签定义样式，尤其是项目初期，涉及到大量扩展的时候，容易由于样式继承造成大量复写

- 背景图片请尽可能使用sprite技术, 减小http请求, 考虑到多人协作开发, sprite按模块制作;




## <a name='format'>顺序与格式</a>

- css属性书写顺序建议:  
  + 自身样式（width,height,border,margin,padding,background）
  + 定位样式（position,top,right,bottom,left,float,z-index,overflow）
  + 其他样式（color,font-size,white-space,box-sizing,display）

- 格式化：如果在模块划分较细的情况下可考虑完全展开

- 代码缩进 2格空格






