#### js 循环相加需要注意的是

1. 在循环体外面定义一个字段【number】类型的字段，不然相加的时候回当成字符串的拼接

2. let num = 0 ，初始化的时候定义为 0 不然会循环相加，当然如果上面的循环的字段本身就是【number】类型的就可以避免循环累加

```js
let num = 0;
data.fees.forEach((i) => {
  if (i.type == 3) {
    num += i.cost_price;
  }
});
```

#### 如果 传值传的是 boolean 值 要这样

```js
  //正确
  result: result == 1 ? true : false

  // 错误的是这样的  这样的是字符串
   result: result == 1 ? 'true' : 'false',

```

#### 逻辑与 与 短路与

- 1== 2 & 2==3 这是逻辑与 1==2 为 felse 会接着走 2==3
- 1==2 && 2==3 这是短路与 1==2 为 false 就不走 2==3

#### less 和 sass 的区别

Less 是基于 JavaScript，是在客户端处理的

Sass 是基于 Ruby 的，是在服务器端处理的。

关于变量在 Less 和 Sass 中 Less 用@，Sass 用$。

因为 Less 与 Sass 处理机制不一样，前者是通过客户端处理的，后者是通过服务端处理，相比较之下 less 会比后者慢一点。

#### 判断 0

```js
num=0

console.log ( num=='' ) true

console.log ( num==='' ) false
```

#### 检测数据类型

```JS
if (typeof num1 === 'number')

	if(data === null)
	if(typeof data === 'string')

typeof  加 ''
	如果直接判断数据 就 null   不加 ''
```
