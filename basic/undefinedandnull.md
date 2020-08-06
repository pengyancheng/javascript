##### Undefined
Undefined类型只有一个值，即特殊的undefined。
在使用var声明变量但未对其加以初始化时，这个变量的值就是undefined
。不过，一般建议尽量给变量初始化，但是在早期的js版本中是没有规定undefined这个值的，
所以在有些框架中为了兼容旧版浏览器，会给window对象添加undefined值。

##### 产生undefined的情况
* 未初始化的变量
* 不存在的对象属性
* 不存在的数组元素

##### Null
Null类型是第二个只有一个值的数据类型，这个特殊的值是null。从逻辑角度来看，null值表示一个空对象指针，而这也正是使用typeof操作符检测null时会返回object的原因。

var car = null;

console.log(typeof car); // "object"

如果定义的变量准备在将来用于保存对象，那么最好将该变量初始化为null而不是其他值。这样一来，只要直接检测null值就可以知道相应的变量是否已经保存了一个对象的引用了。
例如：

if(car != null){

  //对car对象执行某些操作
  
}

实际上，undefined值是派生自null值的，因此ECMA-262规定对它们的相等性测试要返回true。

console.log(undefined == null); //true

尽管null和undefined有这样的关系，但它们的用途完全不同。无论在什么情况下都没有必要把一个变量的值显式地设置为undefined，可是同样的规则对null却不适用。换句话说，只要意在保存对象的变量还没有真正保存对象，就应该明确地让该变量保存null值。这样做不仅可以体现null作为空对象指针的惯例，而且也有助于进一步区分null和undefined。
