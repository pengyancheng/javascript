### typeof

typeof 一般只能返回如下几个结果："number"、"string"、"boolean"、"object"、"function" 和 "undefined"。

运算数为数字 typeof(x) = "number" 

字符串 typeof(x) = "string" 

布尔值 typeof(x) = "boolean" 

对象,数组和null typeof(x) = "object" 

函数 typeof(x) = "function" 


```javascript
console.log(typeof (123)); // 返回"number" 
console.log(typeof ("123")); // 返回"string"
var param1 = "string";
var param2 = new Object();
var param3 = 10;
console.log(typeof(param1)+"\n"+typeof(param2)+"\n"+typeof(param3)); 　　　　　
//　string object  number
```

#### typeof可以用来获取一个变量是否存在，如 if(typeof a!="undefined"){alert("ok")}，而不要去使用 if(a) 因为如果 a 不存在（未声明）则会出错

```javascript
console.log(typeof (a)); // undefined

if(a) {} // 报错
```

typeof在判断null、array、object以及函数实例（new + 函数）时，得到的都是object。这使得在判断这些数据类型的时候，得不到真是的数据类型。由此引出instanceof。

