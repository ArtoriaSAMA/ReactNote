# 🔥🔥🔥对react相关代码库以及框架的源码进行了一定的分析
### ToDo
- [ ] react
    - [x] shared  整个项目通用代码
    - [x] react   核心代码，react定义、reactElement类型对象的构建过程、ReactChildren对react树的操作原理等等
    - [x] react-is  梳理react框架中两大类型：ReactElement以及Portal类型。梳理React.memo，Ref等类型的构建成ReactElementd的过程
    - [x] scheduler 规划 React 初始化，更新等等
    - [x] react-reconciler  React调制器
    - [ ] react-dom  DOM渲染
    - [ ] events 合成事件系统
    - [ ] 各类型组件的运行机制
- [x] react-router4各个API的使用与源码分析
- [ ] react-transition-group
    - [x] 基本组件：Transition组件分析，结合生命周期详细分析该组件实现动画的原理
    - [ ] TransitionGroup组件：对children中Transition或者CSSTransition组件的动画的管理
- [ ] redux-saga：管理react副作用，尽可能使组件为纯函数

## 📖react16.6

<i>源码实例分析：可见[runlogic文件夹](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/runlogic/index.js)下的代码，打log分析react对不同组件的处理逻辑等等运行机制</i>

#### 🍺D1 项目目录
<details>
<summary>View contents</summary>

* [1、react源码浅析(一)：项目目录](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D1/react%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%B8%80)%EF%BC%9A%E9%A1%B9%E7%9B%AE%E7%9B%AE%E5%BD%95.md)
</details>

#### 🍺D2 shared
<details>
<summary>View contents</summary>

- [1、react源码浅析(二)：shared文件夹](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D2/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%ba%8c)%ef%bc%9ashared%e6%96%87%e4%bb%b6%e5%a4%b9.md)
- [2、react源码浅析(二)：shared文件夹之ReactTreeTraversal](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D2/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%ba%8c)%ef%bc%9ashared%e6%96%87%e4%bb%b6%e5%a4%b9%e4%b9%8bReactTreeTraversal.md)
</details>

#### 🍺D3 react
<details>
<summary>View contents</summary>

- [1、react源码浅析(三)：react文件夹-源码入口](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9areact%e6%96%87%e4%bb%b6%e5%a4%b9-%e6%ba%90%e7%a0%81%e5%85%a5%e5%8f%a3.md)
- [2、react源码浅析(三)：ReactNoopUpdateQueue](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactNoopUpdateQueue.md)
- [3、react源码浅析(三)：ReactBaseClasses](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactBaseClasses.md)
- [4、react源码浅析(三)：Ref-Context-Lazy-forwardRef-memo](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aRef-Context-Lazy-forwardRef-memo.md)
- [5、react源码浅析(三)：ReactElement](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactElement.md)
- [6、react源码浅析(三)：ReactDebugCurrentFrame](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactDebugCurrentFrame.md)
- [7、react源码浅析(三)：ReactChildren](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactChildren.md)
- [ ]   8、react源码浅析(三)：Hook
- [9、react源码浅析(三)：ReactElementValidator](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D3/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e4%b8%89)%ef%bc%9aReactElementValidator.md)
</details>


#### 🍺D4 react-is

<i>梳理react中的类型，两大类型的构建过程</i>

<details>
<summary>View contents</summary>

- [react源码浅析(四)：react-is](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D4/react%e6%ba%90%e7%a0%81%e6%b5%85%e6%9e%90(%e5%9b%9b)%ef%bc%9areact-is.md)
</details>

#### 🍺D5 scheduler

<i>scheduler调度器原理，大致基本流程已给出图示，以后再给出更详细具体的调度解析，其实知道了设计思想，往后的内容都基本没问题了。</i>

<i>tracing及其TracingSubscriptions实现的是一个订阅监听者设计模式，暂时不对其总结</i>

<details>
<summary>View contents</summary>

- [react源码浅析(五)：scheduler](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D5/react%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%BA%94)%EF%BC%9Ascheduler.md)
- [react源码浅析(五)：scheduler之Tracing.js](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D5/react%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%BA%94)%EF%BC%9Ascheduler%E4%B9%8BTracing.js.md)
- [react源码浅析(五)：scheduler之TracingSubscriptions.js](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react/blog/D5/react%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%BA%94)%EF%BC%9Ascheduler%E4%B9%8BTracingSubscriptions.js.md)
</details>



#### 🍺D6 react-reconciler

###### <i>react-reconciler源码分析，直接记在我的有道云笔记中，之后会整理成md文件</i>

<details>
<summary>View contents</summary>

- [1、react源码浅析(六)：react的fiber树与页面节点树的关系](http://note.youdao.com/noteshare?id=0f7455578064b5f29fe3078ac8250a52&sub=E75C32B93D164C029A960640C40454A2)
- [2-1、react源码浅析(六)：创建container对应的root](http://note.youdao.com/noteshare?id=5f5fc67ba5ea237fe3c66ffa5f08d6f8&sub=38872ACF66C44A11AAA6D9303AA23523)
- [2-2、react源码浅析(六)：创建root下的fiber树并开始初始调度](http://note.youdao.com/noteshare?id=9e044ed4ed7575202c88b3cfc219fd78&sub=4F5BBFC31A9A417BB16AD3A905941346)
- [2-3、react源码浅析(六)：调度入口函数scheduleWork](http://note.youdao.com/noteshare?id=f0b46b71cf9d0fdc2567c71e73e219cd&sub=13597B790FE74888A94E9A637F47ACA5)
- [2-4、react源码浅析(六)：performWork调度root双向循环链表](http://note.youdao.com/noteshare?id=1ddf559cc188cd1f903801df9ea13c06&sub=C79AC4EE17354E7C8C81F54E46DD9F10)
- [2-5、react源码浅析(六)：performWorkOnRoot调度某个root的fiber树](http://note.youdao.com/noteshare?id=82c1def09e9ab49dc1f7ab12670c077d&sub=461FD4B88C714C4F86F8503DE9236B23)
- [2-6、react源码浅析(六)：渲染阶段renderRoot](http://note.youdao.com/noteshare?id=478f1a3b421050d8f1b72e3b221cca59&sub=169BA6CA7850481BBA68BC53379E26D1)
- [2-7、react源码浅析(六)：提交阶段completeRoot](http://note.youdao.com/noteshare?id=825ff368c0ecd1d1b8526d5d6c3048b5&sub=B99E2F7CE96F4FC495F009DD212DF07C)
</details>



## 📖react-router

#### 🍺D1

<details>
<summary>View contents</summary>

- [react-router4源码浅析(一) ：matchPath](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%B8%80)%20%EF%BC%9AmatchPath.md)
- [react-router4源码浅析(二) ：Route](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%BA%8C)%20%EF%BC%9ARoute.md)
- [react-router4源码浅析(三) ：BrowserRouter&&HashRouter](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%B8%89)%20%EF%BC%9ABrowserRouter%26%26HashRouter.md)
- [react-router4源码浅析(四) ：Router](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E5%9B%9B)%20%EF%BC%9ARouter.md)
- [react-router4源码浅析(五) ：generatePath](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%BA%94)%20%EF%BC%9AgeneratePath.md)
- [react-router4源码浅析(六) ：Redirect](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E5%85%AD)%20%EF%BC%9ARedirect.md)
- [react-router4源码浅析(七) ：Switch](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%B8%83)%20%EF%BC%9ASwitch.md)
- [react-router4源码浅析(八) ：withRouter](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E5%85%AB)%20%EF%BC%9AwithRouter.md)
- [react-router4源码(九) ：Link](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-router/packages/react-router/blog/D1/react-router4%e6%ba%90%e7%a0%81(%e4%b9%9d)+%ef%bc%9aLink.md)
</details>


## 📖react-transition-group

#### 🍺D1

<details>
<summary>View contents</summary>

- [react-transition-group源码浅析(一)：Transition](https://github.com/BUPTlhuanyu/ReactNote/blob/master/react-transition-group/blog/D1/react-transition-group%E6%BA%90%E7%A0%81%E6%B5%85%E6%9E%90(%E4%B8%80)%EF%BC%9ATransition.md)
</details>
