# React_Study

## [七、Redux架构及其实现](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md)

### 作者：冰红茶  
### 参考书籍：《React全栈》 张轩 杨寒星  &&   《深入React技术栈》 陈屹 
### 参考源：[Redux 官网](https://redux.js.org/) 
### [源码地址](https://github.com/hblvsjtu/React_Study/tree/master/reduxtest) 

------    



  之前一直在学React，发现不同组件间的数据传递确实是一个比较麻烦的事情。之前学过Flux，觉得Flux的模式已经是很好的啦，主要思想是建立一个store作为一个中间数据仓库。然后所有的组件的数据存取行为都通过这个数据仓库，减少了不必的行为。但是人总是追求完美和省事，觉得Fluxx的Dispatch都是多余的，想要更高效的框架。于是Redux就诞生了^_ ^
     
## 目录
### [7.1 简介](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.1)
#### [7.1.1 背景和特点](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.1.1)
#### [7.1.2 几个重要的概念](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.1.2)
### [7.2 需要解决的三个问题](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.2)
#### [7.2.1 如何触发reducer](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.2.1)
#### [7.2.2 如何获取state和设置state并更新页面](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.2.2)
#### [7.2.3 有时侯不能更新页面的原因](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.2.3)
### [7.3 中间件Middleware](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.3)
#### [7.3.1 简介](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.3.1)
#### [7.3.2 用途](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.3.2)
### [7.4 在React中如何发挥作用](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.4)
#### [7.4.1 安装插件](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.4.1)
#### [7.4.2 展示型和容器型组件的异同比较](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.4.2)
#### [7.4.3 相关API ](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.4.3)
### [7.4.4 实例](https://github.com/hblvsjtu/React_Study/blob/master/七、Redux架构及其实现.md#7.4.4)
