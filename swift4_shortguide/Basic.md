# The basic 
# 基础
## 变量与常量

### 定义一个常量
```
//不指定类型
let num
//指定类型
let num:Int
```

### 定义一个变量
```
//不指定类型
var firstName
//指定类型
var firstName:String
//变量与常量名支持大部分Unicode名
let 我是中文 = "中文也可以定义变量"
```

### 命名限制

不能包含空格

不能包含数学符号

不能使用保留关键字或已有其它用途的私有Unicode

不能包含 - （横划线）

不能以数字开头

代码注释
```
//代码注释1
/*
* 代码注释2
*/
```
### 分号(;)

单行代码不需要分号(;)
多行需要
```
let num = 10  //不需要分号
let num = 10; let cout = 20 //需要分号
```
### 数据基本类型
Int 整形
```
let A:Int8 //8位整型
let B:Int16 //16位整型
let C:Int32 //32位整型
let D:Int64 //64位整型
let E:Int //默认整型
let F:UInt //默认无符号整形 且 Int及UInt在32位系统上为32位，在64位系统上为64位
```
浮点型
```
let A:Float = 3.14 //float浮点型
let B:Double = 3.14 //double浮点型
let C = 3.14 //不指定，则默认为double
```
类型安全与推断

Swift为类型安全的语言，一旦类型确定，不可更改.没有定义的情况下,Swift会自动推断类型
```
let maxNum = 120 //推断为整型
let pi = 3.14159 //推断为Double型
let sum = 1 + 2.0 //推断为Double型
```
数字表示方式

没有前缀，为十字进
0b开头，为二进制
0o开头，为八进制
0x开头，为十六进制
```
let decimalInteger = 17 //十字进 17
let binaryInteger = 0b10001 //二进制 17
let octalInteger = 0o21 //八进制 17
let hexadecimalInteger = 0x11 //十六进制 17

```
数字类型转换

使用 <b>SomeType(ofInitialValue)</b>进行数字类型的强制转换

整型与整型

```
let A:UInt8 = 2
let B:UInt = 1
let C = (UInt)A + B
```
整形与浮点型

```
let A:Double = 3.14
let B:UInt = 4
let C = (Double)B + A
```

类型别名

允许你为类型定义一个别名，以更符合业务的期望

比如：次数是UInt型，我们定义一个别名

```
typealias Times = UInt
let count:Times = 3 //3次
```
布尔型 (主要用于记录True/False)

```
let example = true
let isGood = false
```
```
if isGood {
  print("Good")
}else{
  print("Bad")
}

```

Tuples 元组 (类似于数组)

Tuples就是把多个同一组的变量值容纳到一个变量中
```
//定义了一个(Int,String)类型的元组
let httpNotFound = (404,"Not Found")
//使用数字来访问元组中的值
let statusCode = httpNotFound.0
let statusDescription = httpNotFound.1
```
或者

你也可以这样定义

```
//定义了一个(Int,String)类型的元组,并给元组中的元素命名
var httpNotFoud:(statusCode:Int,statusDescrption:String) = (404,"Not Found")
//使用元组命名来访问元组中的值
let statusCode = httpNotFoud.statusCode
let statusDescription = httpNotFoud.statusDescrption
```
使用typealias给元组起个别名

```
typealias HttpStatusCode = (statusCode:Int,statusDescrption:String)
var http500Error:HttpStatusCode = (500,"Service Error")
```

Optional

Optioanl表示一个值可能为空，也可能不为空

Android中的闪退，很大一部分比重是与NullPointException(空指针)异常有关

```
//Int? 加？表示Optional ,意味着可以为Int值，也可以为空
var count:Int?
//这是允许的，count为Int?，可以为空
count = nil
```

判断 Optional

```
//第一种，使用 是否 = nil 来判断
var count:Int?
if count != nil {
  print("count is NULL")
}else{
  print("count is not NULL")
}
//第二种，使用 let xxx = 来判断 _ 表示变量省略，(我知道这有个变量，但我不会使用它。。。)
if let _ = count {
  print("count is NULL")
}else{
    print("count is not NULL")
}
```

获取Optional实际的值

```
var aliaName:String?
if let _ = aliaName {
  var name:String = aliaName!
}
```
使用 ! 来将Optional转为背后的对象

Error Handling 错误处理(与OC不同，Swift允许方法定义错误)

```
//这个方法可能会throws错误
func methodA() throws {
}
```
调用者处理错误

```
do {
   try methodA()
}
catch {
  print("发生错误了")
}
```

也可以处理的更细致点

```
do {
  try methodA()
} catch SomeError.error1 {
  
} catch SomeError.error2 {
  
}
```