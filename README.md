# react-入门-lesson
## react 简介
- 组件化
- 分层
- 生态
- 效率（开发、渲染）.UI的变化通过整体刷新改变的.

### react怎么保证局部刷新。

### vdom diff（作业）
- 高效的diff算法，两个vdom的比较；
- vdom是什么？vdom是怎么操作的？
  （vdom:在浏览器端用js实现的一套dom的api,模拟了真正浏览器的dom形成的一套api ;因为它最终用dom去操作，我们要去操作vdom,所以vdom是一个proxy,起到桥接的作用）
  react开发中所有dom构造都是通过vdom进行的，紧接着根据数据变化react会重新构建整个dom树，然后将整个react dom树跟上一次的dom 树进行diff,得到了整个dom树仅仅变更了新的，这就是vdom的普通的渲染过程。
  数据变化的时候，我们利用vdom的方式来对比前后vdom,然后以高性能的方式渲染界面。
- 更新只需要更新节点；
- 数据变化检测，batch dom读写；

### event loop 内两次的数据更新会被合并

### vue && react

- 相同点：
- 都是UI的js库；
- 组件化；
- 都用的vdom;
- 都可以配合webpack做一些单文件等；

- 不同点：
- vue中没有用jsx,用的基于ESNext的模板系统；
- vue的组件有全局组件和局部组件（性能上有什么差异，为什么要提供两个呢？？），react的组件都是通过import引入的；
- props是可以动态变化的；
- 子组件的实时更新；
- react建议props中使用纯函数，同样不建议props中去改变视图，通过state改变视图；
- vue中实现了一些事件的接口，如父子组件通信；react中状态管理必须要引入，除了通过props传，没有特别方便的一些东西；
- vue中computed和watch 语法糖，react无;
- vue的模板系统比较弱，因此引入了指令，react无；
- react all in js ,js 可以操作css, jss style.component;
- redux combineReducer => vuex modules;
- vuex mutation => redux reducer new state immutable;
- react 设计思想：函数式的，推崇纯组件，数据不可变、单向数据流；
- 双向 =》 redux-form;

## JSX
## 元素渲染
## 组件、props、state

### setState原理
- 合成事件、钩子函数 异步 原生事件 setTimeout 同步
- 没有操作渲染，执行了个异步的updateQueue;
- ReactUpdateQueue.js

## react事件机制
onClick={this.handleFunc.bind(this)}
js class

bind/ public class fields, babel

vue-cli => create-react-app
## 生命周期

### 挂载阶段
### update阶段
### 卸载阶段 清楚定时器、取消请求、dom垃圾处理
#### code review 

### react 请求放到didmount,不放在willmount
- 异步
- 多次执行（ssr, react fiber）

## 组件通信
- 父亲-》儿子 props
- 儿子-》父亲 props+callback
- 兄弟组件 找爸爸+找儿子
- 跨层、隔代通信 context
- pub/sub
- 状态管理 (redux mobx)

## 状态提升
> 多个组件需要反映相同变化数据，提升到对应的父组件

1.可变数据，只有一个对应的唯一数据源

## React 如何组织组件复用
- 高阶组件
- render props
- react-hooks

## 引申：mixin、HOC、Hooks
## 备注
- 纯函数/函数式编程/柯里化；
- ReactDOM.render
- fiber源码
- hook
- vdom
