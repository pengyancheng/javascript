### Boolean 转换规则

boolean是JS的6种数据类型(number,string,object,boolean,null,undefined)之一,有且只有两种值:true和false

使用Boolean(value)方法可以强制转换任意值为boolean类型:

```javascript
var message = "false";
var messageAsBoolean = new Boolean(message);
console.log(messageAsBoolean); // true
```

转换规则：取决于转换值得数据类型

|数据类型|转换为true的值|转换为false的值|
|----|----|----|
|Boolean|true|false|
|String|任何非空字符串|空字符串|
|Number|任何非零数字|0和NaN|
|Object|任何对象包括空对象{}|null|
|Undefined|n/a|undefined|
