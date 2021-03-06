美店前端开发规范——UI规范
=====================

### 概述

根据美店第一版的各类使用场景，归纳出目前常用的规范项目，大致分为以下几类：

`1.文本（颜色，字号，修饰等等）`

`2.按钮&标签`

`3.icon`

`4.表单`

`5.特定功能及场景`

`6.控件`

`7.其他`




***

### 1.文本 

- 颜色

  + 默认颜色 $default

  + 链接颜色（默认颜色$link，hover颜色$linkHover）

  + 标题颜色 $title

  + 主色调 $color

  + 次级文字 $grey eg:#666

  + 辅助文字 $tag eg:#999

  + 提示文字 $remind eg:#ccc

- 字号 

  + h1-h5 

  + 内容默认字号

- 字体 

  + 浏览器会自动查找字体库，没有就会跳转到下一个字体，所以这里涉及到一个排序

  + 中文  $font:'Hiragino Sans GB',Microsoft Yahei, tahoma, arial,sans-serif。
  
  + 数字  $number:arial





***

### 2.按钮&标签（此类可直接用代码实现）

- 场景

  + 普通按钮（如选择本页，排序按钮等）

  + 保存，确定，确认，取消

  + 添加，删除
    
  + 标签类（右上角高级版，续费等）

    
- 尺寸

  + 页面级（主要是确定，保存按钮等）

  + 模块级（主要是确定，保存按钮等）

  + 功能级（普通按钮居多，可包含固定多个尺寸）






***


### 3.icon（主要是风格一致，统一的视角、材质，最好能有几个固定的尺寸，满足各类场景，颜色最好不要超过3种）

- 关闭

- 警示类的感叹号（选择商品第一步，第二步的提示；双列宝贝的宝贝展示下的提示）

- 问号（用于对功能的说明）

- 编辑，删除（页面列表）

- 链接（页面列表，链接选择工具）

- 上移，下移，置顶

- 提建议，旺旺





***

### 4.表单

- 输入框

  + 默认宽，高，圆角，修饰等

  + 默认值颜色，字号/默认文案颜色，字号（输入框内）

  + 默认提示（输入框外）

  + 聚焦状态

  + 离开（输入错误）

  + 离开（输入正确）

  + 禁用（默认，hover）

- 确定按钮

  + 默认

  + hover

- 单选按钮，复选按钮






***

### 5.特定功能及场景

- 返回顶部

- 加载更多

- loading图标

- 默认图片

- 进度条（暂无此场景）






***

### 6.控件

- 弹出层popup（商品选择，图片空间等）

- 提示tips（宝贝添加的提示，选择商品标签时的hover后的文案，问号hover后的提示等等）

- 对话框dialog（比如右下角提建议，电话号码等一些弹出层，但交互弱于popup）

- 系统级的弹出框confirm，alert（关闭页面的提示，某些出错时弹出的提示）

- 下拉框（添加宝贝后的店铺分类，每页显示多少条等，这里涉及多级下拉）

- 翻页控件（列表页的翻页，图片空间的翻页，选择商品的翻页等）

- 时间控件（倒计时模块等选时间的场景）

- 搜索框（商品选择里的搜索）

- tab切换（商品选择里的在库，出售中）

- 缩略图
  
  + 包括样式及常用尺寸

  + 场景：图片空间，双列自定义主题

- 警告框（选择商品第一步，第二步的提示；双列宝贝的宝贝展示下的提示，欢迎动画的选择）
  




***

### 7.其他

- 通用线框颜色$border

- 通用区块背景色$bg

- 大模块标题线







