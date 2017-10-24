# The basic operators
# 基础
## 一元运算, 二元运算, 三元运算

Assignment Operator 赋值操作

```
let a = 10
let b = a
print(b)
```
和Object-C不同，Swift的赋值本身不产生值
```
let b = 1
var a:Int
//这种写法是错误的，a = b 本身并不产生值，不能用于if
if a = b {
  //error
}
```