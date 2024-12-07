# OfficialWebsite
超链接工作室官方网站

## 项目概述
|参数|细节|
|----|----|
|模板|vue.js|
|包名称|officialwebsite|
|创建时附加|是否使用 TypeScript 语法、启用 JSX 支持、引入 Vue Router 进行单页面应用开发|

## 推荐集成开发环境设置
[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) （并禁用 Vetur）。

## 在 TS 中为 `.vue` 导入提供类型支持
TypeScript 默认无法处理 `.vue` 导入的类型信息，因此我们用 `vue-tsc` 代替 `tsc` CLI 进行类型检查。在编辑器中，我们需要 [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) 来让 TypeScript 语言服务意识到 `.vue` 类型。

## 自定义配置
参见 [Vite 配置参考](https://vite.dev/config/)。

## 项目设置
```sh
npm install
```

### 为开发而编译和热重载
```sh
npm run dev
```

### 为生产进行类型检查、编译和最小化
```sh
npm run build
```
