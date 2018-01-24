# JavaScript高级程序设计

**重点一**

```
<script type="text/javascript" >
    alert("<\/script>") //要转义不然会报错
</script>
```

**重点二**  
带有src的脚本中的代码是不会被执行的

```
<script type="text/javascript" src="abc">
    alert("<\/script>")


    var message;    // undefined
</script>
```

**重点三**

```
typeof aaaa //如果aaaa没有定义，会返回"undefined"
```

typeof会返回的类型（这也反应了js的基本思想）

* "undefined" -- 如果这个值未定义
* "boolean" -- 如果这个值是布尔值
* "string" -- 如果这个值是字符串
* "number" -- 如果这个值是数值
* "object" -- 如果这个值是对象或null
* "function" -- 如果这个值是函数

**重点四**

Undefined类型只有一个值，即特殊的undefined。在使用var声明变量但未对其加以初始化时，这个变量的值就是undefined, 例如：

```
var message;
alert(message == undefined);  // true
```

**重点五**

Null类型是第二个只有一个值的数据类型，null值表示一个空对象指针，而这也正是使用typeof操作符检测null值会返回"object"的原因

```
var car = null;
alert(typeof car);   // "object"
```

**重点六 Boolean类型转换问题**

| 数据类型 | 转换为true的值 | 转换为false的值 |
| :--- | :--- | :--- |
| Boolean | true | false |
| String | 任何非空字符串 | ""\(空字符串\) |
| Number | 任何非零数字值\(包括无穷大\) | 0和NaN |
| Object | 任何对象 | null |
| Undefined | n/a | undefined |

**重点七 Number类型**

* 八进制字面量在严格模式下是无效的，会导致支持的JavaScript引擎抛出错误
* JavaScript中保存数值的方式，可以保存正零\(+0\) 和 负零 \(-0\)。正零和负零被认为是相等的
* 由于保存浮点数值需要的内存空间是保存整数值的两倍，因此ECMAScript会不失时机地将浮点数值转换为整数值。

```
var floatNum1 = 1.;   // 小数点后面没有数字 -- 解析为1
var floatNum2 = 10.0; // 整数 -- 解析为10
```



