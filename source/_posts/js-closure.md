---
title: JS 闭包特性
date: 2022-02-16 22:52:44
tags:
- js
- JavaScript
- 闭包
category: 学习笔记
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216225920.png
---

之前闭包一直看不懂，最近看了几本书，算是稍微有点感觉了，简单记一下学习成果。

## 为啥要闭包

为了实现封装特性。

## 闭包示例

```JavaScript
var foo = (function() {
    var int = 0
    function change(val) {
        int += val
    }
    return {
        add : function() {
        	change(1)
        },
        red : function() {
            change(-1)
        },
        value : function() {
            return int
        }
    }
})()

foo.add()
foo.add()
console.log(foo.value())
foo.red()
console.log(foo.value())
```

Output:

```plain
2
1
```

这样子就实现了一定程度上的封装，整理一下伪代码，命名上我就用面向对象的术语，方便之后查笔记。

```JavaScript
var 类名 = (function() {
	var 私有成员变量 = 0
	function 私有成员方法(val) {
		成员变量 += val
	}
	return {
		公共方法: function() {
			私有成员方法(1)
		}
		公共Getter : function(){
			return 私有成员变量
		}
	}
})()
类名.公共方法()
终端.打印(类名.公共Getter())
```

## 现代写法

众所周知，JavaScript 是支持面向对象的，那肯定也是支持封装的，那么怎么用面向对象的方法实现呢？

```JavaScript
class Foo {
    value = 0
    change(val) {
        this.value += val
    }
    add() {
        this.change(1)
    }
    red() {
        this.change(-1)
    }
    echo() {
        return this.value
    }
}

var foo = new Foo()
console.log(foo.echo())
```

怎么样？是不是看起来很像 Java？不愧是 'Java'Script 啊。

## 结尾

如此看来，若是只是为了实现封装特性，那就没必要上闭包了，直接上 class 就行，又简单又方便，现在大部分浏览器也支持了
