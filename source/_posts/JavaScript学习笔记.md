---
title: JavaScript学习笔记
date: 2019-07-16 21:22:51
tags:
  - javascript 
  - 学习 
  - 笔记 
  - 前端
categories:
  - 编程入门
---
## javascript
最近在编程时，发现js的基础有点薄弱，特地重新学习了一遍javascript，刚好搭建了博客，就把学习过程中的一些基础与常用知识点记录在此。
<!-- more -->
## 变量
一个变量，就是一个用于存放数值的容器。这个数值可能是一个用于累加计算的数字，或者是一个句子中的字符串。变量的独特之处在于它存放的数值是可以改变的。
**javascript中用var声明变量**
    var x;
    var str;
**初始化变量**
    x=1;
    str='Hello World!';//单双引号几乎没有区别
    str="Hello World!";
### 变量类型
- Number
- String
- Boolean
- Array
- Object

### 其他类型
- Date
- null
- undefined

### javascript中的字符串方法

__将字符串转化为一个数字__
```javascript
    var str='123';
    var num=Number(str);
```
__将数字转化为字符串__
```javascript
    var num=123;
    var str=num.toString();
```
__获得字符串长度__
```javascript
    var str='this is a string';
    str.length;
```
__检索特定字符串字符__
```javascript
    str[0]//从0开始
    str[str.length-1]
```
__从字符串中查找子字符串并提取它__
```javascript
    str.indexOf('is');
```
答案为2，因为is在str内的位置[0,1,2，从第三个字符开始]，若子字符串不在主字符串中，返回-1
知道子字符串的开始和结束位置，可以用**slice()提取**
```javascript
    str.slice(0,4)
```
结果为this，不包括最后一个位置
```javascript
    str.slice(0)
```
结束位置不写则从开始位置提取剩余所有字符
__返回指定索引区间的字符串__
```javascript
    str.substring(x,y)//不包括y
   str.substring(x)//从索引开始到结束
```
__大小写转换__
```javascript
    str.toUpperCase();//转大写
    str.toLowerCase();//转小写
```
__替换字符串某部分__
```javascript
    str.replace('this','test');
```
在实际程序中，想要真正更新browserType变量的值，需要设置变量的值等于刚才的操作结果
```javascript
    strtest=str.replace('this','test');
```
__特殊字符__
反斜杠是一个转义字符
代码|输出
-|-|-
\'|单引号
\"|双引号
\\|反斜杠
\n|换行
\r|回车
\t|tab制表符
\b|退格符
\f|换页符
__其他常用方法__
|方法|描述|
-|-|-
charAt()|返回指定位置的字符
charCodeAt()|返回指定位置字符的unicode值
concat()|连接两个或多个字符串，返回连接后的字符串
fromCharCode()|将unicode转为字符串
### 字符串可以是对象
```javascript
    var str=new String("hello");
    typeof str//返回object
```
### for/in循环
```javascript
    var person={name:'sch',age:'18'};
    for(x in perosn){//x为属性名
        console.log(x);//输出name,age
        console.log(person[x]);//输出sch,18
    }
```


