# Vue 3.0 (进行中...)

## 课程介绍 & HelloWorld

## 编写计数器

## 洗脚城管理系统 欢迎语

## 列表和循环

## 组件化开发

## 06 createApp() & mount()

- `createApp()方法`

创建一个应用

- `mount()方法`

挂载到某个Html的DOM节点上，它接受一个字符串型参数，参数可以使用CSS选择器，一般都是ID选择器的形式，指定挂载的DOM元素

## 07 Vue的生命周期函数-1

生命周期函数可以这样理解：就是**在某一刻会自动执行的函数**。这句话有两个关键此`某一刻` 和 `自动执行`。

``` js
// 被动执行函数
methods: {
    handleItemClick() {
        alert('jspang.com')
    }
},
template: '<h2 v-on:click="handleItemClick">{{message}}</h2>'
```

``` js
// 自动执行函数
mounted() {
    alert('mounted')
}
```

- beforeCreate(): 在实例生成之前会自动执行的函数
- created(): 在实例生成之后会自动执行的函数
- beforeMount(): 在模板渲染完成之前执行的函数
- mounted(): 在模板渲染完成之后执行的函数

``` js
beforeCreate() { console.log('beforeCreate') },
create() { console.log('created') },
beforeMount() { console.log('beforeMount') },
mounted() { console.log('mounted') }
```

## 08 Vue的生命周期函数-2

**beforeUpdate和updated**:

这两个生命周期函数是在Vue中的data数据发生变化时，才会被执行，一个是在变化之前，一个是在变化之后。

**beforUnmount和unmounted生命周期函数**:

这两个生命周期函数是在Vue销毁时自动执行的函数，一个是销毁前执行，一个是销毁后执行。

``` js
  name: '',
  components: {},
  data() {},
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  methods: {},
  destoryed() {}
```

## 09 插值表达式

### 插值表达式是什么？

`字面量`，其实正确的叫法应该叫做`插值表达式`，也就是我们经常看到的`{{ xxxx }}`

### 插值表达式输出html标签和 v-html指令

### 插值表达式只作一次渲染v-once

### 插值表达式中是可以使用JS表达式的

### v-bind指令的使用

## 10 模板动态参数和阻止默认事件

**事件动态绑定:**

``` js
data() {
    return {
        message: 'jspang.com',
        name: 'title',
        event: 'click'
    }
},
template: `
    <h2 @[event]="handleClick" :[name]="message">
        {{ message }}
    </h2>
`
```

**阻止默认事件:**

``` js
methods: {
    handleButton(e) {
        e.preventDefault() // 阻止默认事件 比如form href
    }
}
```

后续会介绍：6种

- stop修饰符 @click.stop
- self修饰符 @click.self
- prevent修饰符 @click.prevent
- capture修饰符 @click.capture
- once修饰符 事件只执行一次
- passive修饰符 解决滚动时性能的修饰符

## 11 模板中使用条件判断

## 12 计算属性-computed

## 13 监听器-watch

## 14 样式绑定详细讲解

## 15 样式绑定-进阶

## 16

## 17

## 18

## 19 [基础]绑定事件详讲-方法和参数

``` js
// @click="addCountClick"
addCountClick() {
    this.count++
}

// @click="addCountClick(3)"
addCountClick(num) {
    this.count += num
}

// 查看事件中event对象
addCountClick(event) {
    this.count++
    console.log(event)
}

// 多个参数的情况下使用event
@click="addCountClick(3, $event)"
addCountClick(num, event) {
    this.count += num
    console.log(event.target)
}
```

一个按钮调用两次方法

``` js
// <button @click="handleBtnClick1(), handleBtnClick2()">增加</button>
// 一次触发两个事件方法，需要用,逗号，把事件隔开，然后每个事件后边必须加上()才能起作用

handleBtnClick1() {
    alert(1)
}
handleBtnClick2() {
    alert(2)
}
```

## 20 [基础]绑定事件详讲-事件修饰符

- stop修饰符 @click.stop
- self修饰符 @click.self
- prevent修饰符 @click.prevent
- capture修饰符 @click.capture
- once修饰符 事件只执行一次
- passive修饰符 解决滚动时性能的修饰符

## 21 [基础]绑定事件详讲-按键、鼠标修饰符

## 22 [基础]表单数据的双绑定-1

- input
- textarea
- checkbox
- radio

## 23 [基础]表单数据的双绑定-2

- checkbox true-value/false-value
- lazy
- number
- trim

## 模板中使用条件判断

## 参考

[技术胖](http://jspang.com/detailed?id=68#toc21)
