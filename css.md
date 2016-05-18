web 前端开发规范-CSS规范
=====================



## <a name='list'>查看其他规范</a>

  + [`页面规范`](./html.md)（html）
  + [`样式规范`](./css.md)（css）
  + [`脚本规范`](./javascript.md)（javascript）
  + [`移动web开发规范`](./mobile.md)
  + [`UI规范`](./ui.md)




## <a name='TOC'>目录</a>

  1. [准备工作](#prepare)
  1. [顺序与格式](#format)
  1. [命名规范](#namespace)
  1. [样式优化](#optimization)




## <a name='prepare'>准备工作</a>

- 书写代码前, 考虑并提高样式重复使用率;

- 背景图片请尽可能使用sprite技术, 减小http请求, 考虑到多人协作开发, sprite按模块制作;

- 项目结构参考 [项目结构](./overview.md#folder)




## <a name='format'>顺序与格式</a>

- css属性书写顺序建议:  
  + 自身样式（width,height,border,margin,padding,background）
  + 定位样式（position,top,right,bottom,left,float,z-index,overflow）
  + 其他样式（color,font-size,white-space,box-sizing,display）

- 格式化：如果在模块划分较细的情况下可考虑完全展开

- 代码缩进 2格空格





## <a name='namespace'>命名规范</a>

- `Class统一用减号"-"连接，ID统一用驼峰式命名`，尽量使用英文**小写**代替拼音，不可以数字开头

- Class使用"类别+功能"的方式命名，如nav-logo,title-tips，使用过程中如发现该样式可复用，则使用"公用前缀+功能"，并放置到对应库文件中

- ID是用来标识具体模块的，所以考虑以功能来命名

- Class命名
  + 表示状态  .on, .action, .selected, .off
  + 表示位置  .first, .last, .main, .side
  + 表示结构  .hd, .bd, .ft, .container, .content
  + 通用元素  .tb, .frm, .nav, .list, .item, .tag, .pic, .info, .tips, -icon


- 样式表命名（网摘）
  + 主要的 master.css 
  + 模块 module.css 
  + 基本共用 base.css 
  + 布局，版面 layout.css 
  + 主题 themes.css 
  + 专栏 columns.css 
  + 文字 font.css 
  + 表单 forms.css 
  + 补丁 mend.css 

- 其他样式命名参考（网摘）

  **页面结构**

  + 容器: container 
  + 页头：header 
  + 内容：content/container 
  + 页面主体：main 
  + 页尾：footer 
  + 导航：nav 
  + 侧栏：sidebar 
  + 栏目：column 
  + 页面外围控制整体布局宽度：wrapper 
  + 左右中：left right center 

  **导航**

  + 导航：nav 
  + 主导航：mainbav 
  + 子导航：subnav 
  + 顶导航：topnav 
  + 边导航：sidebar 
  + 左导航：leftsidebar 
  + 右导航：rightsidebar 
  + 菜单：menu 
  + 子菜单：submenu 
  + 标题: title 
  + 摘要: summary 

  **功能** 
  + 标志：logo 
  + 广告：banner 
  + 登陆：login 
  + 登录条：loginbar 
  + 注册：regsiter 
  + 搜索：search 
  + 功能区：shop 
  + 标题：title 
  + 加入：joinus 
  + 状态：status 
  + 按钮：btn 
  + 滚动：scroll 
  + 标签页：tab 
  + 文章列表：list 
  + 提示信息：msg 
  + 当前的: current 
  + 小技巧：tips 
  + 图标: icon 
  + 注释：note 
  + 指南：guild 
  + 服务：service 
  + 热点：hot 
  + 新闻：news 
  + 下载：download 
  + 投票：vote 
  + 合作伙伴：partner 
  + 友情链接：link 
  + 版权：copyright 





## <a name='optimization'>样式优化</a>

- 尽量不要直接给标签定义样式，尤其是项目初期，涉及到大量扩展的时候，容易由于样式继承造成大量复写

- 使用CSS reset

- 能使用CSS3实现的地方，尽量避免使用切图，低版本浏览器[优雅降级](http://segmentfault.com/q/1010000000264469)

- 避免使用CSS表达式，CSS滤镜，@import样式表

- `合理`使用CSS Sprites 或 BASE64






