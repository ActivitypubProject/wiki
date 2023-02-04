# 技术栈规范

<!-- TOC -->

- [技术栈规范](#技术栈规范)
  - [语言](#语言)
  - [框架](#框架)
  - [样式](#样式)
  - [QA](#qa)
  - [构建(项目构建统一使用@gdjiami/cli)](#构建项目构建统一使用gdjiamicli)
  - [项目管理](#项目管理)
  - [模板引擎](#模板引擎)
  - [开发工具](#开发工具)
  - [nodejs](#nodejs)
  - [utils](#utils)
  - [文档生成](#文档生成)
  - [持续集成](#持续集成)
  - [版本管理](#版本管理)
  - [React 开发规范](#react-开发规范)

<!-- /TOC -->

团队的开发效率是基于稳定且熟练的技术栈。稳定的技术栈规范有利于团队协作和沟通。我们对新的技术是完全开放的，一般而言， 新的技术， 新的解决方案，总是为了更高的生产力而诞生的。 我们容纳一个新的技术选型会有以下几点考虑：

- 学习成本。考虑团队成员的接纳能力。如果成本小于收获的利益，在团队里面推行估计阻力会比较大
- 收益。是否能够解决当前的某些痛点
- 考虑风险。一般我们不会将一个实验阶段的技术使用的生产环境中

## 语言

- ✅ Typescript
- Javascript
  - 需要使用jsdoc进行注释, 推荐[渐进式迁移到Typescript](https://www.typescriptlang.org/docs/handbook/type-checking-javascript-files.html). 在无法运行Typescript的环境也推荐该注释方式

## 框架
- ✅ React
- 备选
  - preact
  - react-native
  - taro(小程序开发)
- 生态
  - 路由
    - react-router
  - 状态管理
    - ✅ react hooks
    - ✅ mobx
    - redux 由于冗余的模板代码，以及不利于Typescript约束，我们已经停止使用该方式.
  - UI框架
    - ✅ antd
      - antd-mobile
    - 备选
      - pile
      - ionic-react
  - 开发模式
    - ✅ react hooks
  - 异步处理
    - rxjs
  - 数据可视化
    - rechart
  - websocket
    - sockjs
  - 地图
    - react-bdmap
  - 图标
    - ✅ svg: 配合`svgr`转换为react组件
    - iconfont

## 样式

- 命名规范
  - BEM
- ✅ CSS-in-js
  - styled-components
- pre-compiler
  - SCSS
- post-compiler
  - PostCSS + env

## QA

- 测试
  - 测试框架
    - [jest](https://jestjs.io/docs/en/tutorial-react)
  - 组件测试
    - [react-testing-library](https://github.com/kentcdodds/react-testing-library)
    - enzyme: react组件测试
  - hooks 测试
    - [react-hooks-testing-library](https://github.com/mpeyper/react-hooks-testing-library)
  - puppeteer: headless chrome

- lint
  - tslint
  - stylelint

- 代码格式化
  - ✅ prettier

## 构建(项目构建统一使用@gdjiami/cli)

- webpack
- rollup
- parcel
- babel
- PWA

## 项目管理

- lerna
- ✅ yarn 统一使用yarn

## 模板引擎

- pug

## 开发工具

- vscode
- cmder: Window端终端模拟器

## nodejs

- express
- sock.js

## utils

- jquery
- lodash

## 文档生成

- docz
- ✅ storybook 
- draw.io: 绘图工具

## 持续集成

- gitlab ci

## 版本管理

- git
  - fork(可视化客户端)

## React 开发规范

- [01 类型检查](https://juejin.im/post/5cd7f2c4e51d453a7d63b715)
- [02 组件的组织](https://juejin.im/post/5cd8fb916fb9a03218556fc1)
- [03 样式的管理](https://juejin.im/post/5cdad9c7f265da039b08915d)
- [04 组件的思维](https://juejin.im/post/5cdc2f54e51d453b0c35930d)
- [05 状态管理](https://juejin.im/post/5ce3ee436fb9a07f070e0220)