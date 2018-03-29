js
===
1.js类型
js5种基本类型： string,boolean,number,null,undefined
js7种数据类型：string,boolean,number,null,undefined,array,object
typeof6种返回格式：'string','number','object','function','boolean','undefined'
2. 获取数组中最大值或最小值的方法：
最大值：Math.min.apply(null,arr);
最小值：Math.min(...[v1,v2……])
3.this:
this的值要等到代码真正执行时才能确定
this的值具体有以下几种情况：
(1)new调用时指的是被构造的对象
(2)call,apply调用，指向我们指定的对象
(3)对象调用，如执行obj.b()，this指向obj
(4)默认的，指向全局变量window（相当于执行window.fun()）
4.Boolean返回值：
Boolean（[]） //true
Boolean(undefined) //false
boolean(null) //false
boolean(0) //false
boolean(NaN) //false
boolean(' ') //false
5.Number转化为0：
Number()
Number(0)
Number(' ')
Number('0')
Number(false)
Number(null)
Number([])
Number([0])