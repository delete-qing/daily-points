## 日常小总结

#### 小点

1. GET，POST，PUT，DELETE 就对应着对这个资源的查 ，改 ，增 ，删 4 个操作。

2. arguments 是一个数组 $event 是个对象

3. 刷新的方法还有$emit 传值的方法还要 pops 不要忘了

4. 在数组查找某个 id 在不在这个数组的时候可以用 includes 这样可以减少循环的次数

5. ...in ...这是遍历对象的 hasOwnProperty 可以找到这个对象中有没有这个可 key 值

6. typeof 可以检查某个数据类型 大多数数用来检查某一个 key 值存不存在 不存在就为 undefined

7. 要获取关于路由的数据可以用 window.localtion 里面的属性可以获取到 域名 ？# 后面的数据

8. 计算不出来数据别急很可能是位置放错了 想要计算总体数据要放到组数据的上一级

9. 根据状态显示按钮的类型 :type="show==2 ? 'primary' : ''" 后面的是一个字符

10. computed 计算属性 可以用来计算数组，状态 要记得使用 多使用计算属性

#### v-model 事件

- 首先传值的时候可以 v-model 数组

- 获取值得时候可以 v-model id，但是这个 id 要做处理

- 在初始化化的时候做处理，可以定义一个空数组，循环初始化给的数组，把数组 push 进去这个临时定义的数组

- 然后把这个临时数组等于初始化的数组 这样 model 初始化的就是 id 传的数据不受影响

- v-model 还可以 model 表格中的 recode.id 用来绑定不同项的不同数据

#### 联级选择器赋值问题：

1. antdesign 中的联级选择器 defaultValue 中的字符串只能是单引号 ，但是 value 选中字符串可以是双引号
2. 这里默认赋值只能是单引号只能用 value
3. 但是可以用 v-model 来赋值 v-model 可以用来赋值编辑这个联级选择器

#### vue3 的组合式 api

1. ref active 都是设置响应式数据的 但是 ref 只能监听简单的数据类型（Number,String,Boolean,Underfined,Null）
2. active 可以监听复杂类型数据（数组、对象 也就是 object）

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
