# The basic 
# 基础
## 变量与常量

### 定义一个常量
<code>
//不指定类型

let num

//指定类型

let num:Int
</code>

### 定义一个变量
<code>
//不指定类型

var firstName

//指定类型

var firstName:String

//变量与常量名支持大部分Unicode名

let 我是中文 = "中文也可以定义变量"

</code>

### 命名限制

不能包含空格

不能包含数学符号

不能使用保留关键字或已有其它用途的私有Unicode

不能包含 - （横划线）

不能以数字开头

代码注释
<code>
//代码注释1

/*

\* 代码注释2

*/
</code>

### 分号(;)

单行代码不需要分号(;)
多行需要

<code>
let num = 10  //不需要分号

let num = 10; let cout = 20 //需要分号
</code>

### 数据基本类型

Int 整形

<code>
let A:Int8 //8位整型

let B:Int16 //16位整型

let C:Int32 //32位整型

let D:Int64 //64位整型

let E:Int //默认整型

let F:UInt //默认无符号整形 且 Int及UInt在32位系统上为32位，在64位系统上为64位
</code>

浮点型
<code>

let A:Float = 3.14 //float浮点型

let B:Double = 3.14 //double浮点型

let C = 3.14 //不指定，则默认为double
</code>

类型安全与推断

Swift为类型安全的语言，一旦类型确定，不可更改.没有定义的情况下,Swift会自动推断类型
<code>

let maxNum = 120 //推断为整型

let pi = 3.14159 //推断为Double型

let sum = 1 + 2.0 //推断为Double型
</code>

数字表示方式

没有前缀，为十字进
0b开头，为二进制
0o开头，为八进制
0x开头，为十六进制

<code>

let decimalInteger = 17 //十字进 17

let binaryInteger = 0b10001 //二进制 17

let octalInteger = 0o21 //八进制 17

let hexadecimalInteger = 0x11 //十六进制 17

</code>

