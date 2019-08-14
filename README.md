# -uncomprehending-javaScript-
Javascript tricks you don't know about


# 讲述你不知道的javaScript


#### 原型  闭包  原型链  事件循环 回调函数  递归


### 1.可怕的console.log


这段代码会在控制台输出什么


![image](https://github.com/Velg03961485/-uncomprehending-javaScript-/blob/master/img/java_1.jpg)


解析：

使用var关键字声明的变量在JavaScript中会被提升，并在内存中开辟空间，由于没有赋值，无法定义数值类型，所以分配默认值undefined。var声明的变量，真正的数值初始化，是发生在你确定赋值的位置。同时，我们要知道，var声明的变量是函数作用域的，也就是我们需要区分局部变量和全局变量，而let和const是块作用域的



```
var a = 10; // 全局作用域，全局变量。a=10
function foo() {
// var a 
//的声明将被提升到到函数的顶部。
// 比如:var a

console.log(a); // 打印 undefined

// 实际初始化值20只发生在这里
   var a = 20; // local scope
}
```


输出的答案是:undefined



