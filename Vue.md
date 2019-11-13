## welcome to Vue

### 全局安装脚手架
```javascript
npm install vue-cli -g //全局安装vue-cli
```
### 使用webpack构建自己的项目
```javascript
vue init webpack yourProject 
```
### 文件配置
```javascript
Project name          //按enter键
Project description	  //按enter键
Author  		          //按enter键
Vue build		          //按enter键
Install vue-router      //是否安装Vue-router 视自己的项目情况而定 一般都是需要的  按enter键
Use ESlint to lint your code   //选择NO  不需要按照严格的代码书写规范
Set up unit tests 	       //选择NO  不需要单元测试
Setup e2e tests with Nightwatch 	 //选择NO   不需要e2e测试
Should we run 'npm install' for you ......  //选择npm或yarn,根据个人情况
```
### 跳回安装的目标项目
```javascript
cd 目标项目地址
```
### 启动项目
> npm  run  dev
### 部分项目配置
修改config/index.js的proxyTable可以配置跨域
修改config/index.js中的17行可以自定义服务启动的端口
