淘维 web 前端开发规范-JS规范
=====================
*美店等项目前端规范*



## <a name='list'>查看其他规范</a>

  + [`页面规范`](./html.md)（html）
  + [`样式规范`](./css.md)（css）
  + [`脚本规范`](./javascript.md)（javascript）
  + [`移动web开发规范`](./mobile.md)



## <a name='TOC'>目录</a>

  1. [命名规范](#namespace)
  1. [语法检查](#syntax)
  1. [模块相关](#module)
  1. [代码细节](#code)
  1. [注释](#comments)




## <a name='namespace'>命名规范</a>

- jQuery 变量要求首字符为$, 私有变量和方法:首字符为_，避免使用全局变量; 

- 变量命名采用 驼峰式命名法 getFirstName
  +匈牙利命名法（s_name）,驼峰式命名法(小驼峰)（getName）,帕斯卡命名法(大驼峰)（GetName）

- 构造器函数首字母大写,如：

  ```javascript

  function Person() {...}

  ```

- 常量全用大写字母，如：

  ```javascript

  var PI = 3.1415926;

  ```

- 私有函数用下划线开头，如：

  ```javascript

  var person = {
    _setSext: function () {
      // ...
    },
    _setName: function () {
      // ...
    }
  };

  ```

- 代码缩进 2格空格




## <a name='syntax'>语法检查</a>

- JS调试使用env.log，线上避免console.log

- 打包前需进行语法检查
  + IDE，编辑器自带语法检查插件
  + jshint jslint等语法检测工具




## <a name='code'>代码细节</a>

- 变量定义
  + 变量统一定义在函数体顶部，使用一个关键字,
  + 声明多个变量时，把不赋值的变量放在后面。

  ```javascript

  //不推荐
  if (n > 0) {
    var a = true;
  }
  //推荐
  var isvalid
  if (n > 0) {
    a = true;
  }

  // 不推荐
  var items = getItems();
  var goSportsTeam = true;
  var dragonball = 'z';

  // 推荐
  var items = getItems(),
      goSportsTeam = true,
      dragonball = 'z';


  // 不推荐
  var i, len, dragonball,
      items = getItems(),
      goSportsTeam = true;

  // 不推荐
  var i, items = getItems(),
      dragonball,
      goSportsTeam = true,
      len;

  // 推荐
  var items = getItems(),
      goSportsTeam = true,
      dragonball,
      length,
      i;

  ```



- 用“===”取代“==”,用!==代替!=。

  前者是严格判断，后者会提前进行隐式的类型转换。

- 花括号{}

  for循环或者if判断等，即使只有一行，也要换行并用{}括起来。

  ```javascript

  //不推荐
  if (condition) statement; 

  //推荐
  if (condition){
    statement;
  }

  ```

- 分号
  语句除了for, function, if, switch, try, while外，必须都有分号结尾

- 避免额外的逗号

  ```javascript

  var arr = [1,2,3,];
  var map = {
    a : 1,
    b : 1,
  };
  
  ```

- 下面类型的对象不建议用new构造：
  + new Number(var num = 0), 
  + new String(var s = ""), 
  + new Boolean(var bool = false), 
  + new Object(var o = {}), 
  + new Array(var arr = [])。
  实例一个对象对性能的损耗大于直接声明一个变量


- 引用对象成员用obj.prop1代替obj[“prop1”]，除非属性名是变量。
  ```javascript
  var luke = {
    jedi: true,
    age: 28
  };

  // 不推荐
  var isJedi = luke['jedi'];

  // 推荐
  var isJedi = luke.jedi;
  ```


- jquery 选择器不要直接使用，先存到一个变量中

  ```javascript

  var $li = $(".products").find(".li");
  $li.each(...);
  $li.find("img").addClass();
  ...

  ```

- 不要使用保留字作为键值，不要把`arguments` 作为一个参数的名字

    ```javascript
    //不推荐
    var superman = {
      default: { clark: 'kent'},
      private: true
    };

    //推荐
    var superman ={
      defaults: { clark: 'kent'},
      hidden: true
    };
    ```


- 使用单引号`''`

    ```javascript
    //不推荐
    var name = "Bob Parr";

    //推荐
    var name = 'Bob Parr';

    //不推荐
    var fullName - "Bob " + this.lastName;

    //推荐
    var fullName = 'Bob ' + this.lastName;
    ```


- 当字符串长度超过80个时，应该通过字符串连接多行显示。

    ```javascript
    //不推荐
    var errorMessage = 'This is a super long error that was thrown because of Batman. When you stop to think about how Batman had anything to do with this, you would get nowhere fast.';

    //不推荐
    var errorMessage = 'This is a super long error that \
    was thrown because of Batman. \
    When you stop to think about \
    how Batman had anything to do \
    with this, you would get nowhere \
    fast.';

    //推荐
    var errorMessage = 'This is a super long error that ' +
      'was thrown because of Batman.' +
      'When you stop to think about ' +
      'how Batman had anything to do ' +
      'with this, you would get nowhere ' +
      'fast.';
    ```






## <a name='comments'>注释</a>

- 使用 `/**...*/` 进行多行注释。注释要包括描述、指定类型、参数值和返回值。

    ```javascript
    // 不推荐

    // make() returns a new element
    // based on the passed in tag name
    //
    // @param <String> tag
    // @return <Element> element
    function make(tag) {

      // ...stuff...

      return element;
    }

    // 推荐
    /**
     * make() returns a new element
     * based on the passed in tag name
     *
     * @param <String> tag
     * @return <Element> element
     */
    function make(tag) {

      // ...stuff...

      return element;
    }
    ```



- 给注释加前缀，比如`FIXME`或`TODO` 
  + 使用 `// FIXME:` 去注释问题

    ```javascript
    function Calculator() {

      // FIXME: shouldn't use a global here
      total = 0;

      return this;
    }
    ```

  + 使用 `// TODO:` 来注释解决方法

    ```javascript
    function Calculator() {

      // TODO: total should be configurable by an options param
      this.total = 0;

      return this;
    }
    ```




## <a name='module'>模块相关</a>

- 设计模式 （目前采用单体+工厂模式，后期考虑中介者模式）

- 模块加载器  requireJS

- 构建工具 grunt（后期切换到gulp）

- 模板  handlebars





参考 ： [javascript style guide](https://github.com/airbnb/javascript)






