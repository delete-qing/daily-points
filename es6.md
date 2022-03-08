# Es6 知识点

### 取值

#### 取值在程序中非常常见，比如从对象 obj 中取值。

```js
const obj = {
  a: 1,
  b: 2,
  c: 3,
  d: 4,
  e: 5,
};

const { a, b, c, d, e } = obj;
```

#### es6 的解构赋值可以这样用

```js
setup(){
    const state =reactive(
        {
            name:'张',
            age:18,
        }
    ),
    const getData=()=>{
       let {name,age} = state
       if(name==18)  return;
    }
}
```

#### 补充

ES6 的解构赋值虽然好用。但是要注意解构的对象不能为 undefined、null。否则会报错，故要给被解构的对象一个默认值。

```js
const { a, b, c, d, e } = obj || {};
```

### 合并数据

#### 比如合并两个数组，合并两个对象。

ES6 的扩展运算符是不是忘记了，还有数组的合并不考虑去重吗？

```js
const a = [1, 2, 3];
const b = [1, 5, 6];
const c = [...new Set([...a, ...b])]; //[1,2,3,5,6]

const obj1 = {
  a: 1,
};
const obj2 = {
  b: 1,
};
const obj = { ...obj1, ...obj2 }; //{a:1,b:1}
```

### 拼接字符串

#### 在${}中可以放入任意的 JavaScript 表达式，可以进行运算，以及引用对象属性。

```js
const name = "小明";
const score = 59;
const result = `${name}${score > 60 ? "的考试成绩及格" : "的考试成绩不及格"}`;
```

### if 中判断

#### ES6 中数组实例方法 includes

```js
const condition = [1, 2, 3, 4];

if (condition.includes(type)) {
  //...
}
```

### 扁平化数组

#### 一个部门 JSON 数据中，属性名是部门 id，属性值是个部门成员 id 数组集合，现在要把有部门的成员 id 都提取到一个数组集合中。

其中使用 Infinity 作为 flat 的参数，使得无需知道被扁平化的数组的维度。

```js
const deps = {
  采购部: [1, 2, 3],
  人事部: [5, 8, 12],
  行政部: [5, 14, 79],
  运输部: [3, 64, 105],
};
let member = Object.values(deps).flat(Infinity);
```
