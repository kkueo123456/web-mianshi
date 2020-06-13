# JAVASCRIPT

- 变量：

  语法：var xxx = xxx;

  变量名的命名规则：可以有数字、字母、下划线组成，不能以数字开头，不能有空格等特殊字符，$除外，区分大小写，驼峰式命名法。

  作用域:局部变量、全局变量

  let、const、var区别？

- 数据类型

  基础类型：Number、String、Boolean、undefined、null

  ​					下列代码，输出值是什么？为什么？

  ​					console.log(a)     //undefined

  ​					var a=10;

  ​					console.log(a)  //10

  ​					变量提升：定义变量的过程会提升到js的顶部，赋值语句还在原位置，所以第一个输出undefined，第二个输出10

  判断基础数据类型：typeof：number、string、boolean、undefined、object

  复杂类型：Object\Function

- 数据类型转换：

  强制类型转换：parseInt()\parseFloat\Number()\Boolean()\String()\toString()

  弱类型转换：+ - * /

- 输出语句：

  console.log()\document.write()

- 弹出语句：

  aler()-----undefined

  confirm()-----确定--true    取消--false

  prompt()----确定--输入的内容   取消--null

- 条件语句（分支语句）

  if..else    if..else if ..else 

  switch..case-------判断是绝对等于。

- 循环语句：

  while    do..while    for   for..in

  其中do..while循环体至少执行一次

- 数组：

  var arr=[]  

  var arr=new Array(4)

  参数为一个数字时：表示长度

  参数为多个值时，表示为数组元素。

  长度：arr.length

  索引：从0开始

  获取/设置：arr[index] = xxx;

  冒泡排序：

- 运算符：

  基础：+ - * /  %

  自增或自减：++  --      a++   ++a

  +=   -=  *=  /=     a+=b----a=a+b

   条件：>   <   >=  <=  == ===   !=  !==

  逻辑运算符：&&    ||   ！

  水仙花数、等腰三角形。。。。

- 函数：

  声明函数：function   xxx(){}

  匿名函数：var fn= function (){}

  立即执行函数：(function(){})()

  全局作用域、局部作用域

  函数不调用不执行。

  return语句：返回一个值或表达式给调用者，之后的语句不执行 ，函数停止。

  闭包：函数内部return一个函数，会将附近的变量一起打包形成一个封闭的环境包，这个环境包就是闭包

  递归函数：函数内部调用函数

- 对象

  创建对象的方法：对象字面量：var obj={}

  ​							  实例化Object:var obj1= new Object()

  ​							  工厂模式

  ​							  构造函数   this.name="tom"   new Fn()

  ​							  原型法：prototype

  ​							  混合法：构造函数：属性   +   原型：方法

  获取对象的属性值:   obj.name    obj["name"]

  设置对象属性值：obj.name="tom"

  遍历对象：for..in     for(var i in obj){}

  ​					i:属性名      obj[i]:属性值

​      var str="dkeh22jxsssshq3":创建一个函数fn，获取字符串中出现次数最多的字符和次数。

```javascript
		var str="sdjwehewuwew";
        var obj={}
        //统计每个字符出现的次数
        for(var i=0;i<str.length;i++){
            if(obj[str[i]]){
                obj[str[i]]++
            }else{
                obj[str[i]]=1
            }
        } 
        console.log(obj)    //每个字符的次数统计结束
        var max=0;
        var maxStr=""
        //求出最大值
        for(var j in obj){
            if(obj[j]>max){
                max=obj[j]
            }
        }
        console.log(max)
		//如果有多个字符串出现次数都是最大的，则判断那个与最大值相同，并拼接
        for(var k in obj){
            if(obj[k]==max){
                maxStr+=k
            }
        }
        console.log(maxStr)
```

- 内置对象：

  Array：属性：length

  ​			 方法：push   pop   shift  unshift

  ​						 join():数组以执行的字符拼接为字符串 

  ​						slice、splice...

  String：属性：length

  ​              方法：charAt    charCodeAt     concat    indexOf    lastIndexOf

  ​						 split():通过指定的符号，拆分字符串为数组

  ​						slice  substr   substring  toLowercase   toUppercase

  ​						replace     match   search.. 

  Math：不需要实例化

  ​			Math.random():生成0-1之间的随机数

  ​			Math.PI      Math.ceil   Math.floor   Math.round....

  Date：日期：new Date()

  ​            getFullYear()    getMonth():0-11   getDate():1-31    getDay():0-6    getHours....

  Number:  toFixed():保留n位小数

  正则：^     $    *  ? +  \d  \w    \s     |     [0-9]    [a-z]  ....

  ​			g:全局    i:不区分大小写

  ​			test()     exec()

- 定时器：异步操作

  setTimeout(fn,1000)

  setInterval

  clearTimeout

  clearInterval(定时器返回值)

- 事件：

  常用事件：onclick   onmouseover   onmouseout...

  event对象：event||window.event

  元素.onclick=function(){

  ​       xxxxx

  }

  添加事件监听：addEventListener('click',fn,true/false)        attachEvent("onclick",fn)

  移除事件监听：removeEventListener("click",fn)                detachEvent("onclick",fn)

  事件冒泡、事件捕获、事件委托、事件穿透

  阻止事件冒泡：stopPropagation()   ie:cancelBubble=true

  阻止默认事件：preventDefault()

- 面向对象：

  编程特点：封装、继承、多态

  ​					抽象、封装、继承

  js继承方式有哪些：

  ​			原型链继承

  ​			构造继承

  ​			实例继承

  ​			组合继承

  ​			寄生继承

- BOM:浏览器对象模型

  window、location、screen、history、navigator

- DOM:文档对象模型

  获取元素的方法：document.getElementById

  通过选择器获取：document.querySelector

  属性：nodeType  nodeValue    nodeName

  节点属性：getAttribute     setAttribute    removAttribute

  DOM操作：创建：createElement   createTextNode

  ​					添加：appendChild

  ​					插入：insertBefore

  ​					移除：removeChild

  ​					复制：cloneNode

  ​					替换：replaceChild

- ajax：原生过程



# ES6：

- let和const

- 解构赋值

  let a=10;let b=5;

  [a,b]=[b,a]

- Set数据结构和Map数据结构

- 内置对象扩展;

  字符：模板字符``

  函数：箭头函数=>    rest参数...arr

  对象：var a=10

  ​			var obj={a}

- class类

  class  xxx{

  ​    constructor(){

   			super()

  ​	}

  }

  class XX extends xxx{}

- promise..then
- catch
- finally

