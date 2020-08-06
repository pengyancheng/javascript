##### Undefined
Undefined类型只有一个值，即特殊的undefined。
在使用var声明变量但未对其加以初始化时，这个变量的值就是undefined
。不过，一般建议尽量给变量初始化，但是在早期的js版本中是没有规定undefined这个值的，
所以在有些框架中为了兼容旧版浏览器，会给window对象添加undefined值。

##### 产生undefined的情况
* 未初始化的变量
* 不存在的对象属性
* 不存在的数组元素
