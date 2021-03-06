**整理进度**：  
- [x] 介绍  
- [x] 目录  
- [ ] ES6  
- [ ] ES7  
- [ ] ES8  
- [ ] ES9  
- [ ] 知识补充  
> 在思考，如何整理好这一份资料，让不同阶段的人，能有不同的收获。  

**更新记录**：  
...前面几天没有写记录。   
* 2018.10.24 添加**ES6**《**Symbol**》和《**Set和Map数据结构**》章节。  
* 2018.10.26 添加**ES6**《**Proxy**》章节。  
* 2018.10.29 添加**ES6**《**正则表达式**》《**Promise**》章节。

**未来规划**：
* 1.将内容按不同模块拆分不同文件，方便README文件的阅读。  
* 2.添加案例项目。  

# 一、介绍
现如今网络上已经有各式各样关于 **ECMAScript** 规范的介绍和分析的文章，而我准备整理一份比较完善也比较精简适合快速入门的资料，主要内容将涵盖**ES6**、**ES7**、**ES8**、**ES9**，如有异议欢迎指点。  
这份资料的**ES6部分**将会参考阮一峰老师的 [ECMAScript6入门](http://es6.ruanyifeng.com/) ，精简和整理出快速实用的内容。  
另外**ES7/ES8/ES9**则会从网络综合参考和整理。   

# 二、目录
<!-- TOC -->

- [一、介绍](#一介绍)
- [二、目录](#二目录)
- [三、正文](#三正文)
    - [1. ES6](#1-es6)
        - [1.1 let 和 const命令](#11-let-和-const命令)
            - [1.1.1 let 命令](#111-let-命令)
            - [1.1.2 const 命令](#112-const-命令)
        - [1.2 变量的解构赋值](#12-变量的解构赋值)
            - [1.2.1 数组](#121-数组)
            - [1.2.2 对象的解构赋值](#122-对象的解构赋值)
            - [1.2.3 字符串的解构赋值](#123-字符串的解构赋值)
            - [1.2.4 数值和布尔值的解构赋值](#124-数值和布尔值的解构赋值)
            - [1.2.5 函数参数的解构赋值](#125-函数参数的解构赋值)
            - [1.2.6 应用](#126-应用)
        - [1.3 字符串的拓展](#13-字符串的拓展)
            - [1.3.1 includes(),startsWith(),endsWith()](#131-includesstartswithendswith)
            - [1.3.2 repeat()](#132-repeat)
            - [1.3.3 padStart(),padEnd()](#133-padstartpadend)
            - [1.3.4 模版字符串](#134-模版字符串)
        - [1.4 正则的拓展](#14-正则的拓展)
            - [1.4.1 介绍](#141-介绍)
            - [1.4.2 字符串的正则方法](#142-字符串的正则方法)
            - [1.4.3 u修饰符](#143-u修饰符)
            - [1.4.4 y修饰符](#144-y修饰符)
            - [1.4.5 flags属性](#145-flags属性)
        - [1.5 数值的拓展](#15-数值的拓展)
            - [1.5.1 Number.isFinite(), Number.isNaN()](#151-numberisfinite-numberisnan)
            - [1.5.2 Number.parseInt(), Number.parseFloat()](#152-numberparseint-numberparsefloat)
            - [1.5.3 Number.isInteger()](#153-numberisinteger)
            - [1.5.4 Math对象的拓展](#154-math对象的拓展)
            - [1.5.5 指数运算符](#155-指数运算符)
        - [1.6 函数的拓展](#16-函数的拓展)
            - [1.6.1 参数默认值](#161-参数默认值)
            - [1.6.2 rest 参数](#162-rest-参数)
            - [1.6.3 name 属性](#163-name-属性)
            - [1.6.4 箭头函数](#164-箭头函数)
            - [1.6.5 双冒号运算符](#165-双冒号运算符)
        - [1.7 数组的拓展](#17-数组的拓展)
            - [1.7.1 拓展运算符](#171-拓展运算符)
            - [1.7.2 Array.from()](#172-arrayfrom)
            - [1.7.3 Array.of()](#173-arrayof)
            - [1.7.4 find()和findIndex()](#174-find和findindex)
            - [1.7.5 fill()](#175-fill)
            - [1.7.6 entries(),keys(),values()](#176-entrieskeysvalues)
            - [1.7.7 includes()](#177-includes)
            - [1.7.8 flat(),flatMap()](#178-flatflatmap)
        - [1.8 对象的拓展](#18-对象的拓展)
            - [1.8.1 属性的简洁表示](#181-属性的简洁表示)
            - [1.8.2 属性名表达式](#182-属性名表达式)
            - [1.8.3 Object.is()](#183-objectis)
            - [1.8.4 Object.assign()](#184-objectassign)
        - [1.9 Symbol](#19-symbol)
            - [1.9.1 介绍](#191-介绍)
            - [1.9.2 更多介绍](#192-更多介绍)
        - [1.10 Set和Map数据结构](#110-set和map数据结构)
            - [1.10.1 Set](#1101-set)
            - [1.10.2 Set的应用](#1102-set的应用)
            - [1.10.3 Map](#1103-map)
            - [1.10.4 Map与其他数据结构互相转换](#1104-map与其他数据结构互相转换)
        - [1.11 Proxy](#111-proxy)
            - [1.11.1 基础使用](#1111-基础使用)
            - [1.11.2 取消Proxy实例](#1112-取消proxy实例)
            - [1.11.3 实现 Web服务的客户端](#1113-实现-web服务的客户端)
        - [1.12 Promise对象](#112-promise对象)
            - [1.12.1 概念](#1121-概念)
            - [1.12.2 基本使用](#1122-基本使用)
            - [1.12.3 Promise.prototype.then()](#1123-promiseprototypethen)
            - [1.12.4 Promise.prototype.catch()](#1124-promiseprototypecatch)
            - [1.12.5 Promise.prototype.finally()](#1125-promiseprototypefinally)
            - [1.12.6 Promise.all()](#1126-promiseall)
            - [1.12.7 Promise.race()](#1127-promiserace)
            - [1.12.8 Promise.resolve()](#1128-promiseresolve)
            - [1.12.9 Promise.reject()](#1129-promisereject)
        - [1.13 Iterator和 for...of循环](#113-iterator和-forof循环)
        - [1.14 Generator函数和应用](#114-generator函数和应用)
        - [1.15 Class语法和继承](#115-class语法和继承)
        - [1.16 Module语法和加载实现](#116-module语法和加载实现)
    - [2. ES7](#2-es7)
        - [Object.keys()，Object.values()，Object.entries()](#objectkeysobjectvaluesobjectentries)
        - [Object.getOwnPropertyDescriptors（）](#objectgetownpropertydescriptors)
    - [3. ES8](#3-es8)
        - [3.1 async函数](#31-async函数)
        - [3.2 Promise.prototype.finally()](#32-promiseprototypefinally)
    - [4. ES9](#4-es9)
        - [4.1 正则表达式 s 修饰符](#41-正则表达式-s-修饰符)
    - [5. 知识补充](#5-知识补充)
        - [5.1 块级作用域](#51-块级作用域)
        - [5.2 ES5/6对数组空位的处理](#52-es56对数组空位的处理)
- [四、结语](#四结语)

<!-- /TOC -->

# 三、正文
## 1. ES6

### 1.1 let 和 const命令

在ES6中，我们通常实用 `let` 表示**变量**，`const` 表示**常量**，并且 `let` 和 `const` 都是**块级作用域**，且在**当前作用域有效**不能重复声明。

#### 1.1.1 let 命令
`let` 命令的用法和 `var` 相似，但是 `let` 只在所在代码块内有效。  
**基础用法**：   
```js
{
    let a = 1;
    let b = 2;
}
```

并且 `let` 有以下特点：  

* **不存在变量提升：**  
在ES6之前，我们 `var` 声明一个**变量**一个**函数**，都会伴随着变量提升的问题，导致实际开发过程经常出现一些逻辑上的疑惑，按照一般思维习惯，变量都是需要先声明后使用。
```js
// var 
console.log(v1); // undefined
var v1 = 2;
// 由于变量提升 代码实际如下
var v1;
console.log(v1)
v1 = 2;

// let 
console.log(v2); // ReferenceError
let v2 = 2;
```

* **不允许重复声明：**  
`let` 和 `const` 在相同作用域下，都**不能重复声明同一变量**，并且**不能在函数内重新声明参数**。
```js
// 1. 不能重复声明同一变量
// 报错
function f1 (){
    let a = 1;
    var a = 2;
}
// 报错
function f2 (){
    let a = 1;
    let a = 2;
}

// 2. 不能在函数内重新声明参数
// 报错
function f3 (a1){
    let a1; 
}
// 不报错
function f4 (a2){
    {
        let a2
    }
}
```

#### 1.1.2 const 命令
`const` 声明一个**只读**的**常量**。  
**基础用法**：  
```js
const PI = 3.1415926;
console.log(PI);  // 3.1415926

```
**注意点**：    
* `const` 声明后，无法修改值；  
```js
const PI = 3.1415926;
PI = 3; 
// TypeError: Assignment to constant variable.
```
* `const` 声明时，必须赋值；  
```js
const a ; 
// SyntaxError: Missing initializer in const declaration.
```
* `const` 声明的常量，`let` 不能重复声明；  
```js
const PI = 3.1415926;
let PI = 0;  
// Uncaught SyntaxError: Identifier 'PI' has already been declared
```

[⬆ 返回目录](#二目录)

### 1.2 变量的解构赋值
**解构赋值概念**：在ES6中，直接从数组和对象中取值，按照对应位置，赋值给变量的操作。  

#### 1.2.1 数组  
**基础用法**：    
```js
// ES6 之前
let a = 1;
let b = 2;

// ES6 之后
let [a, b] = [1, 2];
```

本质上，只要等号两边模式一致，左边变量即可获取右边对应位置的值，更多用法：  

```js
let [a, [[b], c]] = [1, [[2], 3]];
console.log(a, b, c); // 1, 2, 3

let [ , , c] = [1, 2, 3];
console.log(c);       // 3

let [a, , c] = [1, 2, 3];
console.log(a,c);     // 1, 3

let [a, ...b] = [1, 2, 3];
console.log(a,b);     // 1, [2,3]

let [a, b, ..c.] = [1];
console.log(a, b, c); // 1, undefined, []
```

**注意点**：    
* 如果解构不成功，变量的值就等于`undefined`。    
```js
let [a] = [];     // a => undefined
let [a, b] = [1]; // a => 1 , b => undefined
```
* 当左边模式多于右边，也可以解构成功。  
```js
let [a, b] = [1, 2, 3];
console.log(a, b); // 1, 2
```
* 两边模式不同，报错。  
```js
let [a] = 1;
let [a] = false;
let [a] = NaN;
let [a] = undefined;
let [a] = null;
let [a] = {};
```

**指定解构的默认值**：  
**基础用法**：  
```js
let [a = 1] = [];      // a => 1
let [a, b = 2] = [a];  // a => 1 , b => 2
```
特殊情况：  
```js
let [a = 1] = [undefined]; // a => 1
let [a = 1] = [null];      // a => null
```
右边模式对应的值，必须严格等于`undefined`，默认值才能生效，而`null`不严格等于`undefined`。  

#### 1.2.2 对象的解构赋值
与数组解构不同的是，对象解构**不需要严格按照顺序取值**，而只要按照**变量名**去取对应**属性名**的值，若取不到对应**属性名**的值，则为`undefined` 。  

**基础用法**：    
```js
let {a, b} = {a:1, b:2};  // a => 1 , b => 2
let {a, b} = {a:2, b:1};  // a => 2 , b => 1
let {a} = {a:3, b:2, c:1};// a => 3
let {a} = {b:2, c:1};     // a => undefined
```

**注意点**：  
* 若**变量名**和**属性名**不一致，则需要修改名称。
```js
let {a:b} = {a:1, c:2}; 
// error: a is not defined
// b => 1
```
对象的解构赋值的内部机制，是先找到同名属性，然后再赋给对应的变量。真正被赋值的是后者，而不是前者。  
上面代码中，`a` 是匹配的模式，`b`才是变量。真正被赋值的是变量`b`，而不是模式`a`。  

* 对象解构也支持**嵌套解构**。 
```js
let obj = {
    a:[ 1, { b: 2}]
};
let {a, a: [c, {b}]} = obj;
// a=>[1, {b: 2}], b => 2, c => 1
```

**指定解构的默认值**： 
```js
let {a=1} = {};        // a => 1
let {a, b=1} = {a:2};  // a => 2, b => 1

let {a:b=3} = {};      // b => 3
let {a:b=3} = {a:4};   // b = >4
// a是模式，b是变量 牢记

let {a=1} = {a:undefined};  // a => 1
let {a=1} = {a:null};   // a => null
// 因为null与undefined不严格相等，所以赋值有效
// 导致默认值1不会生效。
```

#### 1.2.3 字符串的解构赋值
字符串的解构赋值中，字符串被转换成了一个**类似数组的对象**。 
**基础用法**： 
```js
const [a, b, c, d, e] = 'hello';
a // "h"
b // "e"
c // "l"
d // "l"
e // "o"

let {length:len} = 'hello';// len => 5
```

#### 1.2.4 数值和布尔值的解构赋值
解构赋值的规则是，**只要等号右边的值不是对象或数组，就先将其转为对象**。由于`undefined`和`null`**无法转为对象**，所以对它们进行解构赋值，都会报错。 
```js
// 数值和布尔值的包装对象都有toString属性
let {toString: s} = 123;
s === Number.prototype.toString // true
let {toString: s} = true;
s === Boolean.prototype.toString // true

let { prop: x } = undefined; // TypeError
let { prop: y } = null;      // TypeError
```

#### 1.2.5 函数参数的解构赋值
**基础用法**：  
```js
function fun ([a, b]){
    return a + b;
}
fun ([1, 2]); // 3
```
**指定默认值的解构**: 
```js
function fun ({a=0, b=0} = {}){
    return [a, b];
}
fun ({a:1, b:2}); // [1, 2]
fun ({a:1});      // [1, 0]
fun ({});         // [0, 0]
fun ();           // [0, 0]

function fun ({a, b} = {a:0, b:0}){
    return [a, b];
}
fun ({a:1, b:2}); // [1, 2]
fun ({a:1});      // [1, undefined]
fun ({});         // [undefined, undefined]
fun ();           // [0, 0]
```

#### 1.2.6 应用
* **交换变量的值**: 
```js
let a = 1,b = 2;
[a, b] = [b, a]; // a =>2 , b => 1 
```

* **函数返回多个值**: 
```js
// 返回一个数组
function f (){
    return [1, 2, 3];
}
let [a, b, c] = f(); // a=>1, b=>2, c=>3

// 返回一个对象
function f (){
    return {a:1, b:2};
}
let {a, b} = f();    // a=>1, b=>2
```

* **快速对应参数**: 
快速的将一组参数与变量名对应。 
```js
function f([a, b, c]) {...}
f([1, 2, 3]);

function f({a, b, c}) {...}
f({b:2, c:3, a:1});
```

* **提取JSON数据**： 
```js
let json = {
    name : 'leo',
    age: 18
}
let {name, age} = json;
console.log(name,age); // leo, 18
```

* **遍历Map结构**: 
```js
const m = new Map();
m.set('a':1);
m.set('b':2);
for ([k, v] of m){
    console.log(k + ' : ' + v);
}
// 获取键名
for (let [k] of m){...}
// 获取键值
for (let [,k] of m){...}
```

* **输入模块的指定方法**: 
用于**按需加载**模块中需要用到的方法。 
```js
const {log, sin, cos} = require('math');

```

[⬆ 返回目录](#二目录)


### 1.3 字符串的拓展
#### 1.3.1 includes(),startsWith(),endsWith()
在我们判断字符串是否包含另一个字符串时，ES6之前，我们只有`typeof`方法，ES6之后我们又多了三种方法：   
* **includes()**:返回**布尔值**，表示**是否找到参数字符串**。 
* **startsWith()**:返回**布尔值**，表示参数字符串是否在原字符串的**头部**。 
* **endsWith()**:返回**布尔值**，表示参数字符串是否在原字符串的**尾部**。 
```js
let a = 'hello leo';
a.startsWith('leo');   // false
a.endsWith('o');       // true
a.includes('lo');      // true
```
并且这三个方法都支持第二个参数，表示起始搜索的位置。  
```js
let a = 'hello leo';
a.startsWith('leo',1);   // false
a.endsWith('o',5);       // true
a.includes('lo',6);      // false
```
`endsWith` 是针对前 `n` 个字符，而其他两个是针对从第`n`个位置直到结束。  

#### 1.3.2 repeat()
`repeat`方法返回一个新字符串，表示将原字符串重复`n`次。    
**基础用法**：  
```js
'ab'.repeat(3);        // 'ababab'
'ab'.repeat(0);        // ''
```
**特殊用法**:    
* 参数为`小数`，则取整  
```js
'ab'.repeat(2.3);      // 'abab'
```
* 参数为`负数`或`Infinity`，则报错  
```js
'ab'.repeat(-1);       // RangeError
'ab'.repeat(Infinity); // RangeError
```
* 参数为`0到-1的小数`或`NaN`，则取0  
```js
'ab'.repeat(-0.5);     // ''
'ab'.repeat(NaN);      // ''
```
* 参数为`字符串`，则转成`数字`  
```js
'ab'.repeat('ab');     // ''
'ab'.repeat('3');      // 'ababab'
```

####1.3.3 padStart(),padEnd()
用于将字符串**头部**或**尾部**补全长度，`padStart()`为**头部补全**，`padEnd()`为**尾部补全**。    
这两个方法接收**2个**参数，第一个指定**字符串最小长度**，第二个**用于补全的字符串**。  
**基础用法** ：  
```js
'x'.padStart(5, 'ab');   // 'ababx'
'x'.padEnd(5, 'ab');     // 'xabab'
```
**特殊用法**:  
* 原字符串长度，大于或等于指定最小长度，则返回原字符串。  
```js
'xyzabc'.padStart(5, 'ab'); // 'xyzabc'
```
* 用来补全的字符串长度和原字符串长度之和，超过指定最小长度，则截去超出部分的补全字符串。  
```js
'ab'.padStart(5,'012345'); // "012ab"
```
* 省略第二个参数，则用`空格`补全。  
```js
'x'.padStart(4);           // '    x'
'x'.endStart(4);           // 'x    '
```
#### 1.3.4 模版字符串
用于拼接字符串，ES6之前：  
```js
let a = 'abc' + 
    'def' + 
    'ghi';
```
ES6之后：  
```js
let a = `
    abc
    def
    ghi
`
```
**拼接变量**:
在**反引号(\`)**中使用`${}`包裹变量或方法。  
```js
// ES6之前
let a = 'abc' + v1 + 'def';

// ES6之后
let a = `abc${v1}def`
```

[⬆ 返回目录](#二目录)


### 1.4 正则的拓展
#### 1.4.1 介绍
在ES5中有两种情况。   
* 参数是**字符串**，则第二个参数为正则表达式的修饰符。  
```js
let a = new RegExp('abc', 'i');
// 等价于
let a = /abx/i;
```
* 参数是**正则表达式**，返回一个原表达式的拷贝，且不能有第二个参数，否则报错。   
```js
let a = new RegExp(/abc/i);
//等价于
let a = /abx/i;

let a = new RegExp(/abc/, 'i');
//  Uncaught TypeError
```
ES6中使用：  
第一个参数是正则对象，第二个是指定修饰符，如果第一个参数已经有修饰符，则会被第二个参数覆盖。   
```js
new RegExp(/abc/ig, 'i');
```

#### 1.4.2 字符串的正则方法
常用的四种方法：`match()`、`replace()`、`search()`和`split()`。   

#### 1.4.3 u修饰符
添加`u`修饰符，是为了处理大于`uFFFF`的Unicode字符，即正确处理四个字节的UTF-16编码。   
```js
/^\uD83D/u.test('\uD83D\uDC2A'); // false
/^\uD83D/.test('\uD83D\uDC2A');  // true
```
由于ES5之前不支持四个字节UTF-16编码，会识别为两个字符，导致第二行输出`true`，加入`u`修饰符后ES6就会识别为一个字符，所以输出`false`。   

**注意：**  
加上`u`修饰符后，会改变下面正则表达式的行为：   
* (1)点字符
点字符(`.`)在正则中表示除了**换行符**以外的任意单个字符。对于码点大于`0xFFFF`的Unicode字符，点字符不能识别，必须加上`u`修饰符。   
```js
var a = "𠮷";
/^.$/.test(a);  // false
/^.$/u.test(a); // true
```
* (2)Unicode字符表示法
使用ES6新增的大括号表示Unicode字符时，必须在表达式添加`u`修饰符，才能识别大括号。   
```js
/\u{61}/.test('a');      // false
/\u{61}/u.test('a');     // true
/\u{20BB7}/u.test('𠮷'); // true
```
* (3)量词
使用`u`修饰符后，所有量词都会正确识别码点大于`0xFFFF`的 Unicode 字符。
```js
/a{2}/.test('aa');    // true
/a{2}/u.test('aa');   // true
/𠮷{2}/.test('𠮷𠮷');  // false
/𠮷{2}/u.test('𠮷𠮷'); // true
```
* (4)i修饰符
不加`u`修饰符，就无法识别非规范的`K`字符。  
```js
/[a-z]/i.test('\u212A') // false
/[a-z]/iu.test('\u212A') // true
```

**检查是否设置`u`修饰符：**
使用`unicode`属性。   
```js
const a = /hello/;
const b = /hello/u;

a.unicode // false
b.unicode // true
```

#### 1.4.4 y修饰符
`y`修饰符与`g`修饰符类似，也是全局匹配，后一次匹配都是从上一次匹配成功的下一个位置开始。区别在于，`g`修饰符**只要**剩余位置中存在匹配即可，而`y`修饰符是必须从**剩余第一个**开始。   
```js
var s = 'aaa_aa_a';
var r1 = /a+/g;
var r2 = /a+/y;

r1.exec(s) // ["aaa"]
r2.exec(s) // ["aaa"]

r1.exec(s) // ["aa"]  剩余 '_aa_a'
r2.exec(s) // null
```
**`lastIndex`属性**:
指定匹配的开始位置：   
```js
const a = /a/y;
a.lastIndex = 2;  // 从2号位置开始匹配
a.exec('wahaha'); // null
a.lastIndex = 3;  // 从3号位置开始匹配
let c = a.exec('wahaha');
c.index;          // 3
a.lastIndex;      // 4
```
**返回多个匹配**：  
一个`y`修饰符对`match`方法只能返回第一个匹配，与`g`修饰符搭配能返回所有匹配。   
```js
'a1a2a3'.match(/a\d/y);  // ["a1"]
'a1a2a3'.match(/a\d/gy); // ["a1", "a2", "a3"]
```
**检查是否使用`y`修饰符**：   
使用`sticky`属性检查。   
```js
const a = /hello\d/y;
a.sticky;     // true
```

#### 1.4.5 flags属性
`flags`属性返回所有正则表达式的修饰符。   
```js
/abc/ig.flags;  // 'gi'
```


[⬆ 返回目录](#二目录)


### 1.5 数值的拓展
#### 1.5.1 Number.isFinite(), Number.isNaN()
`Number.isFinite()` 用于检查一个数值是否是有限的，即不是`Infinity`，若参数不是`Number`类型，则一律返回`false` 。    
```js
Number.isFinite(10);            // true
Number.isFinite(0.5);           // true
Number.isFinite(NaN);           // false
Number.isFinite(Infinity);      // false
Number.isFinite(-Infinity);     // false
Number.isFinite('leo');         // false
Number.isFinite('15');          // false
Number.isFinite(true);          // false
Number.isFinite(Math.random()); // true
```

`Number.isNaN()`用于检查是否是`NaN`，若参数不是`NaN`，则一律返回`false`。  
```js
Number.isNaN(NaN);      // true
Number.isNaN(10);       // false
Number.isNaN('10');     // false
Number.isNaN(true);     // false
Number.isNaN(5/NaN);    // true
Number.isNaN('true' / 0);      // true
Number.isNaN('true' / 'true'); // true
```

**区别**：  
与传统全局的`isFinite()`和`isNaN()`方法的区别，传统的这两个方法，是先将参数转换成**数值**，再判断。    
而ES6新增的这两个方法则只对**数值**有效，  `Number.isFinite()`对于**非数值**一律返回`false`,` Number.isNaN()`只有对于`NaN`才返回`true`，其他一律返回`false`。  
```js
isFinite(25);          // true
isFinite("25");        // true
Number.isFinite(25);   // true
Number.isFinite("25"); // false

isNaN(NaN);            // true
isNaN("NaN");          // true
Number.isNaN(NaN);     // true
Number.isNaN("NaN");   // false
```

#### 1.5.2 Number.parseInt(), Number.parseFloat()
这两个方法与全局方法`parseInt()`和`parseFloat()`一致，目的是逐步**减少全局性的方法**，让**语言更模块化**。    
```js
parseInt('12.34');     // 12
parseFloat('123.45#'); // 123.45

Number.parseInt('12.34');     // 12
Number.parseFloat('123.45#'); // 123.45

Number.parseInt === parseInt;     // true
Number.parseFloat === parseFloat; // true
```

#### 1.5.3 Number.isInteger() 
用来判断一个数值是否是整数，若参数不是数值，则返回`false`。    
```js
Number.isInteger(10);   // true
Number.isInteger(10.0); // true
Number.isInteger(10.1); // false
```

#### 1.5.4 Math对象的拓展
ES6新增17个数学相关的**静态方法**，只能在**Math对象**上调用。  
* **Math.trunc**:  
用来去除小数的小数部分，**返回整数部分**。  
若参数为**非数值**，则**先转为数值**。  
若参数为**空值**或**无法截取整数的值**，则返回**NaN**。  
```js
// 正常使用
Math.trunc(1.1);     // 1
Math.trunc(1.9);     // 1
Math.trunc(-1.1);    // -1
Math.trunc(-1.9);    // -1
Math.trunc(-0.1234); // -0

// 参数为非数值
Math.trunc('11.22'); // 11
Math.trunc(true);    // 1
Math.trunc(false);   // 0
Math.trunc(null);    // 0

// 参数为空和无法取整
Math.trunc(NaN);       // NaN
Math.trunc('leo');     // NaN
Math.trunc();          // NaN
Math.trunc(undefined); // NaN
```
**ES5实现**：   
```js
Math.trunc = Math.trunc || function(x){
    return x < 0 ? Math.ceil(x) : Math.floor(x);
}
```

* **Math.sign()**:  
判断一个数是**正数**、**负数**还**是零**，对于非数值，会先转成**数值**。    
返回值：   
    * 参数为正数， 返回 +1
    * 参数为负数， 返回 -1
    * 参数为0， 返回 0
    * 参数为-0， 返回 -0
    * 参数为其他值， 返回 NaN
```js
Math.sign(-1);   // -1
Math.sign(1);    // +1
Math.sign(0);    // 0
Math.sign(-0);   // -0
Math.sign(NaN);  // NaN

Math.sign('');   // 0
Math.sign(true); // +1
Math.sign(false);// 0
Math.sign(null); // 0
Math.sign('9');  // +1
Math.sign('leo');// NaN
Math.sign();     // NaN
Math.sign(undefined); // NaN
```

**ES5实现**  
```js
Math.sign = Math.sign || function (x){
    x = +x;
    if (x === 0 || isNaN(x)){
        return x;
    }
    return x > 0 ? 1: -1;
}
```

* **Math.cbrt()**:  
用来计算一个数的立方根，若参数为非数值则先转成数值。   
```js
Math.cbrt(-1); // -1
Math.cbrt(0);  // 0
Math.cbrt(1);  // 1
Math.cbrt(2);  // 1.2599210498

Math.cbrt('1');   // 1
Math.cbrt('leo'); // NaN
```
**ES5实现**  
```js
Math.cbrt = Math.cbrt || function (x){
    var a = Math.pow(Math.abs(x), 1/3);
    return x < 0 ? -y : y;
}
```

* **Math.clz32()**:  
用于返回一个数的 32 位无符号整数形式有多少个前导 0。    
```js
Math.clz32(0) // 32
Math.clz32(1) // 31
Math.clz32(1000) // 22
Math.clz32(0b01000000000000000000000000000000) // 1
Math.clz32(0b00100000000000000000000000000000) // 2
```

* **Math.imul()**:  
用于返回两个数以 32 位带符号整数形式相乘的结果，返回的也是一个 32 位的带符号整数。    
```js
Math.imul(2, 4)   // 8
Math.imul(-1, 8)  // -8
Math.imul(-2, -2) // 4
```

* **Math.fround()**:  
用来返回一个数的**2位单精度浮点数**形式。  
```js
Math.fround(0)   // 0
Math.fround(1)   // 1
Math.fround(2 ** 24 - 1)   // 16777215
```

* **Math.hypot()**:   
用来返回所有参数的平方和的**平方根**。  
```js
Math.hypot(3, 4);        // 5
Math.hypot(3, 4, 5);     // 7.0710678118654755
Math.hypot();            // 0
Math.hypot(NaN);         // NaN
Math.hypot(3, 4, 'foo'); // NaN
Math.hypot(3, 4, '5');   // 7.0710678118654755
Math.hypot(-3);          // 3
```

* **Math.expm1()**:  
用来返回` ex - 1`，即`Math.exp(x) - 1`。  
```js
Math.expm1(-1) // -0.6321205588285577
Math.expm1(0)  // 0
Math.expm1(1)  // 1.718281828459045
```
**ES5实现**  
```js
Math.expm1 = Math.expm1 || function(x) {
  return Math.exp(x) - 1;
};
```

* **Math.log1p()**:  
用来返回`1 + x`的自然对数，即`Math.log(1 + x)`。如果x小于`-1`，返回`NaN`。  
```js
Math.log1p(1)  // 0.6931471805599453
Math.log1p(0)  // 0
Math.log1p(-1) // -Infinity
Math.log1p(-2) // NaN
```
**ES5实现**  
```js
Math.log1p = Math.log1p || function(x) {
  return Math.log(1 + x);
};
```

* **Math.log10()**:  
用来返回以 `10 `为底的`x的对数`。如果x小于 0，则返回 `NaN`。  
```js
Math.log10(2)      // 0.3010299956639812
Math.log10(1)      // 0
Math.log10(0)      // -Infinity
Math.log10(-2)     // NaN
Math.log10(100000) // 5
```
**ES5实现**  
```js
Math.log10 = Math.log10 || function(x) {
  return Math.log(x) / Math.LN10;
};
```

* **Math.log2()**:  
用来返回以 `2` 为底的`x的对数`。如果`x`小于` 0`，则返回 `NaN`。   
```js
Math.log2(3)       // 1.584962500721156
Math.log2(2)       // 1
Math.log2(1)       // 0
Math.log2(0)       // -Infinity
Math.log2(-2)      // NaN
Math.log2(1024)    // 10
Math.log2(1 << 29) // 29
```
**ES5实现**  
```js
Math.log2 = Math.log2 || function(x) {
  return Math.log(x) / Math.LN2;
};
```
* **双曲函数方法**:  
    * `Math.sinh(x)` 返回x的**双曲正弦**（hyperbolic sine）  
    * `Math.cosh(x)` 返回x的**双曲余弦**（hyperbolic cosine）  
    * `Math.tanh(x)` 返回x的**双曲正切**（hyperbolic tangent）  
    * `Math.asinh(x)` 返回x的**反双曲正弦**（inverse hyperbolic sine）  
    * `Math.acosh(x)` 返回x的**反双曲余弦**（inverse hyperbolic cosine）  
    * `Math.atanh(x)` 返回x的**反双曲正切**（inverse hyperbolic tangent）  

#### 1.5.5 指数运算符
新增的指数运算符(`**`):  
```js
2 ** 2; // 4
2 ** 3; // 8 

2 ** 3 ** 2; // 相当于 2 ** (3 ** 2); 返回 512
```
指数运算符(`**`)与`Math.pow`的实现不相同，对于特别大的运算结果，两者会有细微的差异。
```js
Math.pow(99, 99)
// 3.697296376497263e+197

99 ** 99
// 3.697296376497268e+197
```


[⬆ 返回目录](#二目录)


### 1.6 函数的拓展
#### 1.6.1 参数默认值
```js
// ES6 之前
function f(a, b){
    b = b || 'leo';
    console.log(a, b);
}

// ES6 之后
function f(a, b='leo'){
    console.log(a, b);
}

f('hi');          // hi leo
f('hi', 'jack');  // hi jack
f('hi', '');      // hi leo
```
**注意**:  
* 参数变量是默认声明的，不能用`let`和`const`再次声明：    
```js
function f (a = 1){
    let a = 2; // error
}
```
* 使用参数默认值时，参数名不能相同：  
```js
function f (a, a, b){ ... };     // 不报错
function f (a, a, b = 1){ ... }; // 报错
```

**与解构赋值默认值结合使用**：  
```js
function f ({a, b=1}){
    console.log(a,b)
};
f({});         // undefined 1
f({a:2});      // 2 1
f({a:2, b:3}); // 2 3
f();           // 报错

function f ({a, b = 1} = {}){
    console.log(a, b)
}
f();  // undefined 1
```

**尾参数定义默认值**:   
通常在尾参数定义默认值，便于观察参数，并且非尾参数无法省略。 
```js
function f (a=1,b){
    return [a, b];
}
f();    // [1, undefined]
f(2);   // [2, undefined]
f(,2);  // 报错

f(undefined, 2);  // [1, 2]

function f (a, b=1, c){
    return [a, b, c];
}
f();        // [undefined, 1, undefined]
f(1);       // [1,1,undefined]
f(1, ,2);   // 报错
f(1,undefined,2); // [1,1,2]
```
在给参数传递默认值时，传入`undefined`会触发默认值，传入`null`不会触发。  
```js
function f (a = 1, b = 2){
    console.log(a, b);
}
f(undefined, null); // 1 null
```

**函数的length属性**:  
`length`属性将返回，没有指定默认值的参数数量，并且rest参数不计入`length`属性。    
```js
function f1 (a){...};
function f2 (a=1){...};
function f3 (a, b=2){...};
function f4 (...a){...};
function f5 (a,b,...c){...};

f1.length; // 1
f2.length; // 0
f3.length; // 1
f4.length; // 0
f5.length; // 2
```

#### 1.6.2 rest 参数
`rest`参数形式为（`...变量名`），其值为一个数组，用于获取函数多余参数。  
```js
function f (a, ...b){
    console.log(a, b);
}
f(1,2,3,4); // 1 [2, 3, 4]
```
**注意**：  
* `rest`参数只能放在最后一个，否则报错：  
```js
function f(a, ...b, c){...}; // 报错 
```
* 函数的`length`属性不包含`rest`参数。
```js
function f1 (a){...};
function f2 (a,...b){...};
f1(1);   // 1
f2(1,2); // 1
```

#### 1.6.3 name 属性
用于返回该函数的函数名。  
```js
function f (){...};
f.name;    // f

const f = function g(){...};
f.name;    // g
```

#### 1.6.4 箭头函数
使用“箭头”(`=>`)定义函数。  
**基础使用**：   
```js
// 有1个参数
let f = v => v;
// 等同于
let f = function (v){return v};

// 有多个参数
let f = (v, i) => {return v + i};
// 等同于
let f = function (v, i){return v + i};

// 没参数
let f = () => 1;
// 等同于
let f = function (){return 1};
```

**箭头函数与变量结构结合使用**：  
```js
// 正常函数写法
function f (p) {
    return p.a + ':' + p.b;
}

// 箭头函数写法
let f = ({a, b}) => a + ':' + b;
```

**简化回调函数**：  
```js
// 正常函数写法
[1, 2, 3].map(function (x){
    return x * x;
})


// 箭头函数写法
[1, 2, 3].map(x => x * x);
```

**箭头函数与rest参数结合**：  
```js
let f = (...n) => n;
f(1, 2, 3); // [1, 2, 3]
```

**注意点**：   
* 1.箭头函数内的`this`**总是**指向**定义时所在的对象**，而不是调用时。  
* 2.箭头函数不能当做**构造函数**，即不能用`new`命令，否则报错。  
* 3.箭头函数不存在`arguments`对象，即不能使用，可以使用`rest`参数代替。  
* 4.箭头函数不能使用`yield`命令，即不能用作**Generator**函数。   

**不适用场景**：  
* 1.在定义函数方法，且该方法内部包含`this`。  
```js
const obj = {
    a:9,
    b: () => {
        this.a --;
    }
}
```
上述`b`如果是**普通函数**，函数内部的`this`指向`obj`，但是如果是箭头函数，则`this`会指向**全局**，不是预期结果。  

* 2.需要动态`this`时。  
```js
let b = document.getElementById('myID');
b.addEventListener('click', ()=>{
    this.classList.toggle('on');
})
```
上诉按钮点击会报错，因为`b`监听的箭头函数中，`this`是全局对象，若改成**普通函数**，`this`就会指向被点击的按钮对象。  

#### 1.6.5 双冒号运算符
双冒号暂时是一个提案，用于解决一些不适用的场合，取代`call`、`apply`、`bind`调用。    
双冒号运算符(`::`)的左边是一个**对象**，右边是一个**函数**。该运算符会自动将左边的对象，作为上下文环境(即`this`对象)，绑定到右边函数上。  
```js
f::b;
// 等同于
b.bind(f);

f::b(...arguments);
// 等同于
b.apply(f, arguments);
```
若双冒号左边为空，右边是一个对象的方法，则等于将该方法绑定到该对象上。  
```js
let f = a::a.b;
// 等同于
let f = ::a.b;
```

[⬆ 返回目录](#二目录)


### 1.7 数组的拓展
#### 1.7.1 拓展运算符
拓展运算符使用(`...`)，类似`rest`参数的逆运算，将数组转为用(`,`)分隔的参数序列。   
```js
console.log(...[1, 2, 3]);   // 1 2 3 
console.log(1, ...[2,3], 4); // 1 2 3 4
```
拓展运算符主要使用在函数调用。  
```js
function f (a, b){
    console.log(a, b);
}
f(...[1, 2]); // 1 2

function g (a, b, c, d, e){
    console.log(a, b, c, d, e);
}
g(0, ...[1, 2], 3, ...[4]); // 0 1 2 3 4
```
**若拓展运算符后面是个空数组，则不产生效果**。  
```js
[...[], 1]; // 1
```

**替代apply方法**  
```js
// ES6之前
function f(a, b, c){...};
var a = [1, 2, 3];
f.apply(null, a);

// ES6之后
function f(a, b, c){...};
let a = [1, 2, 3];
f(...a);

// ES6之前
Math.max.apply(null, [3,2,6]);

// ES6之后
Math.max(...[3,2,6]);
```

**拓展运算符的运用** 
* **(1)复制数组**：  
通常我们直接复制数组时，只是浅拷贝，如果要实现深拷贝，可以使用拓展运算符。  
```js
// 通常情况 浅拷贝
let a1 = [1, 2];
let a2 = a1; 
a2[0] = 3;
console.log(a1,a2); // [3,2] [3,2]

// 拓展运算符 深拷贝
let a1 = [1, 2];
let a2 = [...a1];
// let [...a2] = a1; // 作用相同
a2[0] = 3;
console.log(a1,a2); // [1,2] [3,2]
```
* **(2)合并数组**：  
注意，这里合并数组，只是浅拷贝。  
```js
let a1 = [1,2];
let a2 = [3];
let a3 = [4,5];

// ES5 
let a4 = a1.concat(a2, a3);

// ES6
let a5 = [...a1, ...a2, ...a3];

a4[0] === a1[0]; // true
a5[0] === a1[0]; // true
```
* **(3)与解构赋值结合**：  
与解构赋值结合生成数组，但是使用拓展运算符需要放到参数最后一个，否则报错。   
```js
let [a, ...b] = [1, 2, 3, 4]; 
// a => 1  b => [2,3,4]

let [a, ...b] = [];
// a => undefined b => []

let [a, ...b] = ["abc"];
// a => "abc"  b => []
```

#### 1.7.2 Array.from()
将 **类数组对象** 和 **可遍历的对象**，转换成真正的数组。  
```js
// 类数组对象
let a = {
    '0':'a',
    '1':'b',
    length:2
}
let arr = Array.from(a);

// 可遍历的对象
let a = Array.from([1,2,3]);
let b = Array.from({length: 3});
let c = Array.from([1,2,3]).map(x => x * x);
let d = Array.from([1,2,3].map(x => x * x));
```

#### 1.7.3 Array.of()
将一组数值，转换成**数组**，弥补`Array`方法参数不同导致的差异。   
```js
Array.of(1,2,3);    // [1,2,3]
Array.of(1).length; // 1

Array();       // []
Array(2);      // [,] 1个参数时，为指定数组长度
Array(1,2,3);  // [1,2,3] 多于2个参数，组成新数组
```

#### 1.7.4 find()和findIndex()
`find()`方法用于找出第一个符合条件的数组成员，参数为一个回调函数，所有成员依次执行该回调函数，返回第一个返回值为`true`的成员，如果没有一个符合则返回`undefined`。  
```js
[1,2,3,4,5].find( a => a < 3 ); // 1
```
回调函数接收三个参数，当前值、当前位置和原数组。  
```js
[1,2,3,4,5].find((value, index, arr){
    // ...
});
```
`findIndex()`方法与`find()`类似，返回第一个符合条件的数组成员的**位置**，如果都不符合则返回`-1`。  
```js
[1,2,3,4].findIndex((v,i,a)=>{
    return v>2;
}); // 2
```

#### 1.7.5 fill()
用于用指定值**填充**一个数组，通常用来**初始化空数组**，并抹去数组中已有的元素。   
```js
new Array(3).fill('a');   // ['a','a','a']
[1,2,3].fill('a');        // ['a','a','a']
```
并且`fill()`的第二个和第三个参数指定填充的**起始位置**和**结束位置**。   
```js
[1,2,3].fill('a',1,2);
```

#### 1.7.6 entries(),keys(),values()
主要用于遍历数组，`entries()`对键值对遍历，`keys()`对键名遍历，`values()`对键值遍历。   
```js
for (let i of ['a', 'b'].keys()){
    console.log(i)
}
// 0
// 1

for (let e of ['a', 'b'].keys()){
    console.log(e)
}
// 'a'
// 'b'

for (let e of ['a', 'b'].keys()){
    console.log(e)
}
// 0 'a'
// 1 'b'
```

#### 1.7.7 includes()
用于表示数组是否包含给定的值，与字符串的`includes`方法类似。   
```js
[1,2,3].includes(2);     // true
[1,2,3].includes(4);     // false
[1,2,NaN].includes(NaN); // true
```
第二个参数为**起始位置**，默认为`0`，如果负数，则表示倒数的位置，如果大于数组长度，则重置为`0`开始。  
```js
[1,2,3].includes(3,3);    // false
[1,2,3].includes(3,4);    // false
[1,2,3].includes(3,-1);   // true
[1,2,3].includes(3,-4);   // true
```

#### 1.7.8 flat(),flatMap()
`flat()`用于将数组一维化，返回一个新数组，不影响原数组。   
默认一次只一维化一层数组，若需多层，则传入一个整数参数指定层数。   
若要一维化所有层的数组，则传入`Infinity`作为参数。  
```js
[1, 2, [2,3]].flat();        // [1,2,2,3]
[1,2,[3,[4,[5,6]]]].flat(3); // [1,2,3,4,5,6]
[1,2,[3,[4,[5,6]]]].flat('Infinity'); // [1,2,3,4,5,6]
```
`flatMap()`是将原数组每个对象先执行一个函数，在对返回值组成的数组执行`flat()`方法，返回一个新数组，不改变原数组。  
 `flatMap()`只能展开一层。  
```js
[2, 3, 4].flatMap((x) => [x, x * 2]); 
// [2, 4, 3, 6, 4, 8] 
```

[⬆ 返回目录](#二目录)


### 1.8 对象的拓展
#### 1.8.1 属性的简洁表示
```js
let a = 'a1';
let b = { a };  // b => { a : 'a1' }
// 等同于
let b = { a : a };

function f(a, b){
    return {a, b}; 
}
// 等同于
function f (a, b){
    return {a:a ,b:b};
}

let a = {
    fun () {
        return 'leo';
    }
}
// 等同于
let a = {
    fun : function(){
        return 'leo';
    }
}
```

#### 1.8.2 属性名表达式
`JavaScript`提供2种方法**定义对象的属性**。  
```js
// 方法1 标识符作为属性名
a.f = true;

// 方法2 字符串作为属性名
a['f' + 'un'] = true;
```
延伸出来的还有：   
```js
let a = 'hi leo';
let b = {
    [a]: true,
    ['a'+'bc']: 123,
    ['my' + 'fun'] (){
        return 'hi';
    }
};
// b.a => undefined ; b.abc => 123 ; b.myfun() => 'hi'
// b[a] => 'hi leo' ; b['abc'] => 123 ; b['myfun'] => 'hi'
```
**注意**：  
属性名表达式不能与简洁表示法同时使用，否则报错。   
```js
// 报错
let a1 = 'aa';
let a2 = 'bb';
let b1 = {[a1]};

// 正确
let a1 = 'aa';
let b1 = { [a1] : 'bb'};
```

#### 1.8.3 Object.is()
`.Object.is()` 用于比较两个值是否严格相等，在ES5时候只要使用**相等运算符**(`==`)和**严格相等运算符**(`===`)就可以做比较，但是它们都有缺点，前者会**自动转换数据类型**，后者的`NaN`不等于自身，以及`+0`等于`-0`。   
```js
Object.is('a','a');   // true
Object.is({}, {});    // false

// ES5
+0 === -0 ;           // true
NaN === NaN;          // false

// ES6
Object.is(+0,-0);     // false
Object.is(NaN,NaN);   // true
```

#### 1.8.4 Object.assign()
`Object.assign()`方法用于对象的合并，将原对象的所有可枚举属性复制到目标对象。  
**基础用法**：  
第一个参数是**目标对象**，后面参数都是**源对象**。  
```js
let a = {a:1};
let b = {b:2};
Object.assign(a,b);  // a=> {a:1,b:2}
```
**注意**：  
* 若目标对象与源对象有同名属性，则后面属性会覆盖前面属性。  
```js
let a = {a:1, b:2};
let b = {b:3, c:4};
Object.assign(a, b); // a => {a:1, b:3, c:4}
```
* 若只有**一个**参数，则返回该参数。 
```js
let a = {a:1};
Object.assign(a) === a;  // true
```
* 若参数**不是对象**，则先转成对象后返回。
```js
typeof Object.assign(2); // 'object'
```
* 由于`undefined`或`NaN`无法转成对象，所以做为参数会报错。   
```js
Object.assign(undefined) // 报错
Object.assign(NaN);      // 报错
```
* `Object.assign()`实现的是浅拷贝。   

`Object.assign()`拷贝得到的是这个对象的引用。这个对象的任何变化，都会反映到目标对象上面。
```js
let a = {a: {b:1}};
let b = Object.assign({},a);
a.a.b = 2;
console.log(b.a.b);  // 2
```
* 将数组当做对象处理，键名为数组下标，键值为数组下标对应的值。
```js
Object.assign([1, 2, 3], [4, 5]); // [4, 5, 3]
```

[⬆ 返回目录](#二目录)


### 1.9 Symbol
#### 1.9.1 介绍
ES6引入`Symbol`作为一种新的**原始数据类型**，表示**独一无二**的值，主要是为了**防止属性名冲突**。   
ES6之后，JavaScript一共有其中数据类型：`Symbol`、`undefined`、`null`、`Boolean`、`String`、`Number`、`Object`。  
简单实用：   
```js
let a = Symbol();
typeof a; // "symbol"
```
**注意：**  
* `Symbol`函数不能用`new`，会报错。由于`Symbol`是一个原始类型，不是对象，所以不能添加属性，它是类似于字符串的数据类型。   
* `Symbol`都是不相等的，即使参数相同。   
```js
let a1 = Symbol();
let a2 = Symbal();
a1 === a2; // false 

let a1 = Symbol('abc');
let a2 = Symbal('abc');
a1 === a2; // false 
```
* `Symbol`不能与其他类型的值计算，会报错。   
```js
let a = Symbol('hello');
a + " world!";  // 报错
`${a} world!`;  // 报错
```

#### 1.9.2 更多介绍
详细介绍[参考阮一峰老师的ES6 Symbol介绍](http://es6.ruanyifeng.com/#docs/symbol)


[⬆ 返回目录](#二目录)


### 1.10 Set和Map数据结构  
#### 1.10.1 Set
**介绍**:   
`Set`数据结构类似数组，但所有成员的值**唯一**。  
`Set`本身为一个构造函数，用来生成`Set`数据结构，使用`add`方法来添加新成员。      
```js
let a = new Set();
[1,2,2,1,3,4,5,4,5].forEach(x=>a.add(x));
for(let k of a){
    console.log(k)
};
// 1 2 3 4 5
```
**基础使用**：  
```js
let a = new Set([1,2,3,3,4]);
[...a]; // [1,2,3,4]
a.size; // 4

// 数组去重
[...new Set([1,2,3,4,4,4])];// [1,2,3,4]
```

**注意**：   
* 向`Set`中添加值的时候，不会类型转换，即`5`和`'5'`是不同的。   
```js
[...new Set([5,'5'])]; // [5, "5"]
```

**属性和方法**：   
* 属性：  
    * `Set.prototype.constructor`：构造函数，默认就是`Set`函数。   
    * `Set.prototype.size`：返回`Set`实例的成员总数。  

* 操作方法：  
    * `add(value)`：添加某个值，返回 Set 结构本身。  
    * `delete(value)`：删除某个值，返回一个布尔值，表示删除是否成功。  
    * `has(value)`：返回一个布尔值，表示该值是否为Set的成员。  
    * `clear()`：清除所有成员，没有返回值。  

```js
let a = new Set();
a.add(1).add(2); // a => Set(2) {1, 2}
a.has(2);        // true
a.has(3);        // false
a.delete(2);     // true  a => Set(1) {1}
a.clear();       // a => Set(0) {}
```
**数组去重**：   
```js
let a = new Set([1,2,3,3,3,3]);
```
#### 1.10.2 Set的应用
**数组去重**：  
```js
// 方法1
[...new Set([1,2,3,4,4,4])]; // [1,2,3,4]
// 方法2
Array.from([1,2,3,4,4,4]);   // [1,2,3,4]
```
**遍历和过滤**：  
```js
let a = new Set([1,2,3,4]);

// map 遍历操作
let b = new Set([...a].map(x =>x*2));// b => Set(4) {2,4,6,8}

// filter 过滤操作
let c = new Set([...a].filter(x =>(x%2) == 0)); // b => Set(2) {2,4}
```
**获取并集、交集和差集**：   
```js
let a = new Set([1,2,3]);
let b = new Set([4,3,2]);

// 并集
let c1 = new Set([...a, ...b]);  // Set {1,2,3,4}

// 交集
let c2 = new Set([...a].filter(x => b.has(x))); // set {2,3}

// 差集
let c3 = new Set([...a].filter(x => !b.has(x))); // set {1,4}
```

* 遍历方法：  
    * `keys()`：返回**键名**的遍历器。  
    * `values()`：返回**键值**的遍历器。  
    * `entries()`：返回**键值对**的遍历器。  
    * `forEach()`：使用回调函数遍历**每个成员**。  

`Set`遍历顺序是**插入顺序**，当保存多个回调函数，只需按照顺序调用。但由于`Set`结构**没有键名只有键值**，所以`keys()`和`values()`是返回结果相同。  
```js
let a = new Set(['a','b','c']);
for(let i of a.keys()){console.log(i)};   // 'a' 'b' 'c'
for(let i of a.values()){console.log(i)}; // 'a' 'b' 'c'
for(let i of a.entries()){console.log(i)}; 
// ['a','a'] ['b','b'] ['c','c']
```
并且 还可以使用`for...of```直接遍历`Set`。  
```js
let a = new Set(['a','b','c']);
for(let k of a){console.log(k)};   // 'a' 'b' 'c'
```
`forEach`与数组相同，对每个成员执行操作，且无返回值。  
```js
let a = new Set(['a','b','c']);
a.forEach((v,k) => console.log(k + ' : ' + v));
```


#### 1.10.3 Map
由于传统的`JavaScript`对象只能用字符串当做键，给开发带来很大限制，ES6增加`Map`数据结构，使得**各种类型的值**(包括对象)都可以作为键。   
`Map`结构提供了“**值—值**”的对应，是一种更完善的 Hash 结构实现。
**基础使用**：  
```js
let a = new Map();
let b = {name: 'leo' };
a.set(b,'my name'); // 添加值
a.get(b);           // 获取值
a.size;      // 获取总数
a.has(b);    // 查询是否存在
a.delete(b); // 删除一个值
a.clear();   // 清空所有成员 无返回
```
**注意**：  
* 传入数组作为参数，**指定键值对的数组**。   
```js
let a = new Map([
    ['name','leo'],
    ['age',18]
])
```
* 如果对同一个键**多次赋值**，后面的值将**覆盖前面的值**。   
```js
let a = new Map();
a.set(1,'aaa').set(1,'bbb');
a.get(1); // 'bbb'
```
* 如果读取一个未知的键，则返回`undefined`。  
```js
new Map().get('abcdef'); // undefined
```
* **同样的值**的两个实例，在 Map 结构中被视为两个键。   
```js
let a = new Map();
let a1 = ['aaa'];
let a2 = ['aaa'];
a.set(a1,111).set(a2,222);
a.get(a1); // 111
a.get(a2); // 222
```
**遍历方法**：
Map 的遍历顺序就是插入顺序。  
* `keys()`：返回键名的遍历器。
* `values()`：返回键值的遍历器。
* `entries()`：返回所有成员的遍历器。
* `forEach()`：遍历 Map 的所有成员。
```js
let a = new Map([
    ['name','leo'],
    ['age',18]
])

for (let i of a.keys()){...};
for (let i of a.values()){...};
for (let i of a.entries()){...};
a.forEach((v,k,m)=>{
    console.log(`key:${k},value:${v},map:${m}`)
})
```
**将Map结构转成数组结构**：  
```js
let a = new Map([
    ['name','leo'],
    ['age',18]
])

let a1 = [...a.keys()];   // a1 => ["name", "age"]
let a2 = [...a.values()]; // a2 =>  ["leo", 18]
let a3 = [...a.entries()];// a3 => [['name','leo'], ['age',18]]
```

#### 1.10.4 Map与其他数据结构互相转换
* Map 转 数组  
```js
let a = new Map().set(true,1).set({f:2},['abc']);
[...a]; // [[true:1], [ {f:2},['abc'] ]]
```
* 数组 转 Map  
```js
let a = [ ['name','leo'], [1, 'hi' ]]
let b = new Map(a);
```
* Map 转 对象
如果所有 Map 的键都是字符串，它可以无损地转为对象。   
如果有非字符串的键名，那么这个键名会被转成字符串，再作为对象的键名。   
```js
function fun(s) {
  let obj = Object.create(null);
  for (let [k,v] of s) {
    obj[k] = v;
  }
  return obj;
}

const a = new Map().set('yes', true).set('no', false);
fun(a)
// { yes: true, no: false }
```
* 对象 转 Map   
```js
function fun(obj) {
  let a = new Map();
  for (let k of Object.keys(obj)) {
    a.set(k, obj[k]);
  }
  return a;
}

fun({yes: true, no: false})
// Map {"yes" => true, "no" => false}
```

* Map 转 JSON   
**(1)Map键名都是字符串，转为对象JSON：**   
```js
function fun (s) {
    let obj = Object.create(null);
    for (let [k,v] of s) {
        obj[k] = v;
    }
    return JSON.stringify(obj)
}
let a = new Map().set('yes', true).set('no', false);
fun(a);
// '{"yes":true,"no":false}'
```
**(2)Map键名有非字符串，转为数组JSON：**    
```js
function fun (map) {
  return JSON.stringify([...map]);
}

let a = new Map().set(true, 7).set({foo: 3}, ['abc']);
fun(a)
// '[[true,7],[{"foo":3},["abc"]]]'
```
* JSON 转 Map  
**(1)所有键名都是字符串：**   
```js
function fun (s) {
  let strMap = new Map();
  for (let k of Object.keys(s)) {
    strMap.set(k, s[k]);
  }
  return strMap;
  return JSON.parse(strMap);
}
fun('{"yes": true, "no": false}')
// Map {'yes' => true, 'no' => false}
```
**(2)整个 JSON 就是一个数组，且每个数组成员本身，又是一个有两个成员的数组**:   
```js
function fun2(s) {
  return new Map(JSON.parse(s));
}
fun2('[[true,7],[{"foo":3},["abc"]]]')
// Map {true => 7, Object {foo: 3} => ['abc']}
```

[⬆ 返回目录](#二目录)


### 1.11 Proxy
`proxy` 用于修改某些操作的**默认行为**，可以理解为一种拦截外界对目标对象访问的一种机制，从而对外界的访问进行过滤和修改，即代理某些操作，也称“**代理器**”。   
#### 1.11.1 基础使用  
`proxy`实例化需要传入两个参数，`target`参数表示所要拦截的目标对象，`handler`参数也是一个对象，用来定制拦截行为。   
```js
let p = new Proxy(target, handler);

let a = new Proxy({}, {
    get: function (target, handler){
        return 'leo';
    }
})
a.name; // leo
a.age;  // leo
a.abcd; // leo
```
上述`a`实例中，在第二个参数中定义了`get`方法，来拦截外界访问，并且`get`方法接收两个参数，分别是**目标对象**和**所要访问的属性**，所以不管外部访问对象中任何属性都会执行`get`方法返回`leo`。   
**注意**：   
* 只能使用`Proxy`实例的对象才能使用这些操作。  
* 如果`handler`没有设置拦截，则直接返回原对象。  
```js
let target = {};
let handler = {};
let p = new Proxy(target, handler);
p.a = 'leo'; 
target.a;  // 'leo'
```
**同个拦截器函数，设置多个拦截操作**：  
```js
let p = new Proxy(function(a, b){
    return a + b;
},{
    get:function(){
        return 'get方法';
    },
    apply:function(){
        return 'apply方法';
    }
})
```

**`Proxy`支持的13种拦截操作**：   
13种拦截操作的详细介绍：[打开阮一峰老师的链接](http://es6.ruanyifeng.com/#docs/proxy)。   
* `get(target, propKey, receiver)`：
拦截对象属性的读取，比如proxy.foo和proxy['foo']。

* `set(target, propKey, value, receiver)`：
拦截对象属性的设置，比如proxy.foo = v或proxy['foo'] = v，返回一个布尔值。

* `has(target, propKey)`：
拦截propKey in proxy的操作，返回一个布尔值。

* `deleteProperty(target, propKey)`：
拦截delete proxy[propKey]的操作，返回一个布尔值。

* `ownKeys(target)`：
拦截Object.getOwnPropertyNames(proxy)、Object.getOwnPropertySymbols(proxy)、Object.keys(proxy)、for...in循环，返回一个数组。该方法返回目标对象所有自身的属性的属性名，而Object.keys()的返回结果仅包括目标对象自身的可遍历属性。

* `getOwnPropertyDescriptor(target, propKey)`：
拦截Object.getOwnPropertyDescriptor(proxy, propKey)，返回属性的描述对象。

* `defineProperty(target, propKey, propDesc)`：
拦截Object.defineProperty(proxy, propKey, propDesc）、Object.defineProperties(proxy, propDescs)，返回一个布尔值。

* `preventExtensions(target)`：
拦截Object.preventExtensions(proxy)，返回一个布尔值。

* `getPrototypeOf(target)`：
拦截Object.getPrototypeOf(proxy)，返回一个对象。

* `isExtensible(target)`：
拦截Object.isExtensible(proxy)，返回一个布尔值。

* `setPrototypeOf(target, proto)`：
拦截Object.setPrototypeOf(proxy, proto)，返回一个布尔值。如果目标对象是函数，那么还有两种额外操作可以拦截。

* `apply(target, object, args)`：
拦截 Proxy 实例作为函数调用的操作，比如proxy(...args)、proxy.call(object, ...args)、proxy.apply(...)。

* `construct(target, args)`：
拦截 Proxy 实例作为构造函数调用的操作，比如new proxy(...args)。

#### 1.11.2 取消Proxy实例
使用`Proxy.revocale`方法取消`Proxy`实例。   
```js
let a = {};
let b = {};
let {proxy, revoke} = Proxy.revocale(a, b);

proxy.name = 'leo';  // 'leo'
revoeke();
proxy.name;  // TypeError: Revoked
```

#### 1.11.3 实现 Web服务的客户端
```js
const service = createWebService('http://le.com/data');
service.employees().than(json =>{
    const employees = JSON.parse(json);
})

function createWebService(url){
    return new Proxy({}, {
        get(target, propKey, receiver{
            return () => httpGet(url+'/'+propKey);
        })
    })
}
```

### 1.12 Promise对象
#### 1.12.1 概念
主要用途：**解决异步编程带来的回调地狱问题**。   
把`Promise`简单理解一个容器，存放着某个未来才会结束的事件（通常是一个异步操作）的结果。通过`Promise`对象来获取异步操作消息，处理各种异步操作。   

**`Promise`对象2特点**：  
* **对象的状态不受外界影响**。
> `Promise`对象代表一个异步操作，有三种状态：**pending（进行中）**、**fulfilled（已成功）**和**rejected（已失败）**。只有异步操作的结果，可以决定当前是哪一种状态，任何其他操作都无法改变这个状态。这也是`Promise`这个名字的由来，它的英语意思就是“承诺”，表示其他手段无法改变。

* **一旦状态改变，就不会再变，任何时候都可以得到这个结果**。  
> Promise对象的状态改变，只有两种可能：从**pending**变为**fulfilled**和从**pending**变为**rejected**。只要这两种情况发生，状态就凝固了，不会再变了，会一直保持这个结果，这时就称为 **resolved**（已定型）。如果改变已经发生了，你再对**Promise**对象添加回调函数，也会立即得到这个结果。这与事件（Event）完全不同，事件的特点是，如果你错过了它，再去监听，是得不到结果的。      

注意，为了行文方便，本章后面的`resolve`d统一只指`fulfilled`状态，不包含`rejected`状态。

**`Promise`缺点**   
* **无法取消**Promise，一旦新建它就会立即执行，无法中途取消。  
* 如果不设置回调函数，Promise内部抛出的错误，不会反应到外部。
* 当处于pending状态时，无法得知目前进展到哪一个阶段（刚刚开始还是即将完成）。

#### 1.12.2 基本使用
`Promise`为一个构造函数，需要用`new`来实例化。   
```js
let p = new Promise(function (resolve, reject){
   if(/*异步操作成功*/){
       resolve(value);
   } else {
       reject(error);
   }
})
```
`Promise`接收一个函数作为参数，该函数两个参数`resolve`和`reject`，有JS引擎提供。   
* `resolve`作用是将`Promise`的状态从pending变成resolved，在异步操作成功时调用，返回异步操作的结果，作为参数传递出去。    
* `reject`作用是将`Promise`的状态从pending变成rejected，在异步操作失败时报错，作为参数传递出去。   

`Promise`实例生成以后，可以用`then`方法分别指定`resolved`状态和`rejected`状态的回调函数。   
```js
p.then(function(val){
    // success...
},function(err){
    // error...
})
```

**几个例子来理解** ： 
* 当一段时间过后，`Promise`状态便成为`resolved`触发`then`方法绑定的回调函数。  
```js
function timeout (s){
    return new Promise((resolve, reject){
        setTimeout(result,ms, 'done');
    })
}
timeout(100).then(val => {
    console.log(val);
})
```

* `Promise`新建后立刻执行。 
```js 
let p = new Promise(function(resolve, reject){
    console.log(1);
    resolve();
})
p.then(()=>{
    console.log(2);
})
console.log(3);
// 1
// 2
// 3 
```

**异步加载图片**：  
```js
function f(url){
    return new Promise(function(resolve, reject){
        const img = new Image ();
        img.onload = function(){
            resolve(img);
        }
        img.onerror = function(){
            reject(new Error(
                'Could not load image at ' + url
            ));
        }
        img.src = url;
    })
}
```

**`resolve`函数和`reject`函数的参数为`resolve`函数或`reject`函数**：  
`p1`的状态决定了`p2`的状态，所以`p2`要等待`p1`的结果再执行回调函数。  
```js
const p1 = new Promise(function (resolve, reject) {
  setTimeout(() => reject(new Error('fail')), 3000)
})

const p2 = new Promise(function (resolve, reject) {
  setTimeout(() => resolve(p1), 1000)
})

p2
  .then(result => console.log(result))
  .catch(error => console.log(error))
// Error: fail
```

**调用`resolve`或`reject`不会结束`Promise`参数函数的执行，除了`return`**:     
```js
new Promise((resolve, reject){
    resolve(1);
    console.log(2);
}).then(r => {
    console.log(3);
})
// 2
// 1

new Promise((resolve, reject){
    return resolve(1);
    console.log(2);
})
// 1
```

#### 1.12.3 Promise.prototype.then()
作用是为`Promise`添加状态改变时的回调函数，`then`方法的第一个参数是`resolved`状态的回调函数，第二个参数（可选）是`rejected`状态的回调函数。   
`then`方法返回一个新`Promise`实例，与原来`Promise`实例不同，因此可以使用链式写法，上一个`then`的结果作为下一个`then`的参数。  
```js
getJSON("/posts.json").then(function(json) {
  return json.post;
}).then(function(post) {
  // ...
});
```

#### 1.12.4 Promise.prototype.catch()
`Promise.prototype.catch`方法是`.then(null, rejection)`的别名，用于指定发生错误时的回调函数。   
```js
getJSON('/posts.json').then(function(posts) {
  // ...
}).catch(function(error) {
  // 处理 getJSON 和 前一个回调函数运行时发生的错误
  console.log('发生错误！', error);
});
```
如果 `Promise` 状态已经变成`resolved`，再抛出错误是无效的。   
```js
const p = new Promise(function(resolve, reject) {
  resolve('ok');
  throw new Error('test');
});
p
  .then(function(value) { console.log(value) })
  .catch(function(error) { console.log(error) });
// ok
```
当`promise`抛出一个错误，就被`catch`方法指定的回调函数捕获，下面三种写法相同。   
```js
// 写法一
const p = new Promise(function(resolve, reject) {
  throw new Error('test');
});
p.catch(function(error) {
  console.log(error);
});
// Error: test

// 写法二
const p = new Promise(function(resolve, reject) {
  try {
    throw new Error('test');
  } catch(e) {
    reject(e);
  }
});
p.catch(function(error) {
  console.log(error);
});

// 写法三
const p = new Promise(function(resolve, reject) {
  reject(new Error('test'));
});
p.catch(function(error) {
  console.log(error);
});
```
一般来说，不要在`then`方法里面定义` Reject` 状态的回调函数（即`then`的第二个参数），总是使用`catch`方法。    
```js
// bad
promise
  .then(function(data) {
    // success
  }, function(err) {
    // error
  });

// good
promise
  .then(function(data) { //cb
    // success
  })
  .catch(function(err) {
    // error
  });
```

#### 1.12.5 Promise.prototype.finally()
`finally`方法用于指定不管 `Promise` 对象最后状态如何，都会执行的操作。该方法是 ES2018 引入标准的。   
```js
promise
.then(result => {···})
.catch(error => {···})
.finally(() => {···});
```
`finally`不接收任何参数，与状态无关，本质上是`then`方法的特例。   
```js
promise
.finally(() => {
  // 语句
});

// 等同于
promise
.then(
  result => {
    // 语句
    return result;
  },
  error => {
    // 语句
    throw error;
  }
);
```
上面代码中，如果不使用`finally`方法，同样的语句需要为成功和失败两种情况各写一次。有了`finally`方法，则只需要写一次。   
`finally`方法总是会返回原来的值。   
```js
// resolve 的值是 undefined
Promise.resolve(2).then(() => {}, () => {})

// resolve 的值是 2
Promise.resolve(2).finally(() => {})

// reject 的值是 undefined
Promise.reject(3).then(() => {}, () => {})

// reject 的值是 3
Promise.reject(3).finally(() => {})
```

#### 1.12.6 Promise.all() 
用于将多个 `Promise` 实例，包装成一个新的 `Promise` 实例，参数可以不是数组，但必须是Iterator接口，且返回的每个成员都是`Promise`实例。  
```js
const p = Promise.all([p1, p2, p3]);
```
`p`的状态由`p1`、`p2`、`p3`决定，分成**两种**情况。  
1. 只有p1、p2、p3的状态都变成fulfilled，p的状态才会变成fulfilled，此时p1、p2、p3的返回值组成一个数组，传递给p的回调函数。  
2. 只要p1、p2、p3之中有一个被rejected，p的状态就变成rejected，此时第一个被reject的实例的返回值，会传递给p的回调函数。   

```js
// 生成一个Promise对象的数组
const promises = [2, 3, 5, 7, 11, 13].map(function (id) {
  return getJSON('/post/' + id + ".json");
});

Promise.all(promises).then(function (posts) {
  // ...
}).catch(function(reason){
  // ...
});
```
上面代码中，`promises`是包含 6 个 Promise 实例的数组，只有这 6 个实例的状态都变成`fulfilled`，或者其中有一个变为`rejected`，才会调用`Promise.all`方法后面的回调函数。    

**注意**：如果`Promise`的参数中定义了`catch`方法，则`rejected`后不会触发`Promise.all()`的`catch`方法，因为参数中的`catch`方法执行完后也会变成`resolved`，当`Promise.all()`方法参数的实例都是`resolved`时就会调用`Promise.all()`的`then`方法。   
```js
const p1 = new Promise((resolve, reject) => {
  resolve('hello');
})
.then(result => result)
.catch(e => e);

const p2 = new Promise((resolve, reject) => {
  throw new Error('报错了');
})
.then(result => result)
.catch(e => e);

Promise.all([p1, p2])
.then(result => console.log(result))
.catch(e => console.log(e));
// ["hello", Error: 报错了]
```

**如果参数里面都没有catch方法，就会调用Promise.all()的catch方法。**   
```js
const p1 = new Promise((resolve, reject) => {
  resolve('hello');
})
.then(result => result);

const p2 = new Promise((resolve, reject) => {
  throw new Error('报错了');
})
.then(result => result);

Promise.all([p1, p2])
.then(result => console.log(result))
.catch(e => console.log(e));
// Error: 报错了
```

#### 1.12.7 Promise.race()
与`Promise.all`方法类似，也是将多个`Promise`实例包装成一个新的`Promise`实例。   
```js
const p = Promise.race([p1, p2, p3]);
```
与`Promise.all`方法区别在于，`Promise.race`方法是`p1`, `p2`, `p3`中只要一个参数先改变状态，就会把这个参数的返回值传给`p`的回调函数。  

#### 1.12.8 Promise.resolve()
将现有对象转换成 `Promise` 对象。   
```js
const p = Promise.resolve($.ajax('/whatever.json'));
```

#### 1.12.9 Promise.reject()
返回一个`rejected`状态的`Promise`实例。  
```js
const p = Promise.reject('出错了');
// 等同于
const p = new Promise((resolve, reject) => reject('出错了'))

p.then(null, function (s) {
  console.log(s)
});
// 出错了
```
注意，`Promise.reject()`方法的参数，会原封不动地作为`reject`的理由，变成后续方法的参数。这一点与`Promise.resolve`方法不一致。   
```js
const thenable = {
  then(resolve, reject) {
    reject('出错了');
  }
};

Promise.reject(thenable)
.catch(e => {
  console.log(e === thenable)
})
// true
```


[⬆ 返回目录](#二目录)

### 1.13 Iterator和 for...of循环

[⬆ 返回目录](#二目录)

### 1.14 Generator函数和应用

[⬆ 返回目录](#二目录)

### 1.15 Class语法和继承

[⬆ 返回目录](#二目录)

### 1.16 Module语法和加载实现

[⬆ 返回目录](#二目录)


## 2. ES7
### Object.keys()，Object.values()，Object.entries() 
[对应地址](http://es6.ruanyifeng.com/#docs/object#Object-assign)

[⬆ 返回目录](#二目录)

### Object.getOwnPropertyDescriptors（）

[对应地址](http://es6.ruanyifeng.com/#docs/object#Object-assign)

[⬆ 返回目录](#二目录)

## 3. ES8
### 3.1 async函数
[对应地址](http://es6.ruanyifeng.com/#docs/async)

### 3.2 Promise.prototype.finally()
[对应地址](http://es6.ruanyifeng.com/#docs/promise)

## 4. ES9
### 4.1 正则表达式 s 修饰符
[对应地址](http://es6.ruanyifeng.com/#docs/regex)


[⬆ 返回目录](#二目录)

## 5. 知识补充
### 5.1 块级作用域

通常指一个**函数内部**，或者一个**代码块内部**。  
比如：  
```js
function fun1 () {
    // 块级作用域
    if (true) {
        // 块级作用域
    }
}
```
**缺点**：
1.导致内层变量覆盖外层变量
```js
var a1 = new Date();
function f1 (){
    console.log(a1); // undefined
    if (false) {
        var a1 = 'hello'
    }
}
```
输出 `undefined` 是因为 `if` 内的 `a1` 变量声明的变量提升，导致内部的 `a1` 覆盖外部的 `a1`，所以输出为 `undefined` 。 

2.变量的全局污染
```js
var a = 'hello';
for (var i = 0; i< a.length; i++) {
    //...
}
console.log(i); // 5
```
循环结束后，变量 `i` 的值依然存在，造成变量的全局污染。


[⬆ 返回目录](#二目录)


### 5.2 ES5/6对数组空位的处理

数组的空位不是`undefined`，而是没有任何值，数组的`undefined`也是有值。  
```js
0 in [undefined,undefined,undefined] // true
0 in [,,,] // false
```
**ES5对空位的处理**：  
* `forEach()`, `filter()`, `reduce()`, `every()` 和`some()`都会跳过空位。  
* `map()`会跳过空位，但会保留这个值。  
* `join()`和`toString()`会将空位视为`undefined`，而`undefined`和`null`会被处理成空字符串。  
```js
[,'a'].forEach((x,i) => console.log(i)); // 1
['a',,'b'].filter(x => true);      // ['a','b']
[,'a'].every(x => x==='a');        // true
[1,,2].reduce((x,y) => x+y);       // 3
[,'a'].some(x => x !== 'a');       // false
[,'a'].map(x => 1);                // [,1]
[,'a',undefined,null].join('#');   // "#a##"
[,'a',undefined,null].toString();  // ",a,,"
```
**ES6对空位的处理**：  
将空位视为正常值，转成`undefined`。
```js
Array.from(['a',,'b']);// [ "a", undefined, "b" ]
[...['a',,'b']];       // [ "a", undefined, "b" ]

//copyWithin() 会连空位一起拷贝。  
[,'a','b',,].copyWithin(2,0) // [,"a",,"a"]

//fill()会将空位视为正常的数组位置。
new Array(3).fill('a') // ["a","a","a"]

//for...of循环也会遍历空位。
let arr = [, ,];
for (let i of arr) {
  console.log(1);
}  // 1 1
```
`entries()`、`keys()`、`values()`、`find()`和`findIndex()`会将空位处理成`undefined`。   
```js
[...[,'a'].entries()] // [[0,undefined], [1,"a"]]

[...[,'a'].keys()] // [0,1]

[...[,'a'].values()] // [undefined,"a"]

[,'a'].find(x => true) // undefined

[,'a'].findIndex(x => true) // 0
```
**由于空位的处理规则非常不统一，所以建议避免出现空位。**


# 四、结语

[回到顶部](#一介绍)
