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

11. 若是要改变字符串的分隔符 可以用 replaceAll 方法 a=a.repaceAll（‘，’，‘~’）这样就好了

12. BEM 命名规范 （Block Element Modifier） 就是 css 规范

13. js 的默认属性 $event arguments 找不到属性可以往这里面找 要仔细看 因为属性特别多

14. 有时候一个事件 根据状态的不同调用接口/方法 如果直接调的话不行 可以换种思路 多写个方法只传值 然后接口可以在写一个方法 也就是把这些方法拆开 一个事件有个方法 而不是一个方法一个事件 有封装的思想也要有有拆开的思想

15. - .env 是要加入代码版本管理的
    - .env.local 本地运行的环境
    - 这两个要保证变量名一致 若有需要加别的变量名需要说的

16. 日常忘记日期的转化 i.value.format("HH:mm:ss") 对象转为字符串

17. 初始化数据 range: data.range || [],

18. vue antdesign 下拉框改变方向 :getPopupContainer="trigger => trigger.parentNode"

19. 为什么获取数组某一条值用的是 arr[0]而不是 arr.0，是因为在 JavaScript 中，以数字开头的属性不能用点号引用，必须用方括号。

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

