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

## 09 插值表达式

### 插值表达式是什么？

`字面量`，其实正确的叫法应该叫做`插值表达式`，也就是我们经常看到的`{{ xxxx }}`

### 插值表达式输出html标签和 v-html指令

### 插值表达式只作一次渲染v-once

### 插值表达式中是可以使用JS表达式的

### v-bind指令的使用

## 参考

[技术胖](http://jspang.com/detailed?id=68#toc21)
