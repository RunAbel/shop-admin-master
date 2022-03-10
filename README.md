# 商城后台管理项目

> Vue 3 + Typescript + Vite

## 随记

- 项目采用[vite](https://cn.vitejs.dev/)来进行构建打包
- vite并没有集成eslint，需要自行[添加](https://eslint.org/docs/user-guide/getting-started),并配置eslint验证规则以此来适配vue3
- 编辑器集成
  - 如果vscode插件安装有vetur(vue2代码校验插件) 需禁用
  - 安装 ESLint、Vue Language Features (Volar) 插件，并手动配置并启用
- 安装配置 git commit hook
  > 在提交前自动运行link，杜绝不符合规范的代码进入库中
  - [husky](https://github.com/typicode/husky)
  - [lint-staged](https://github.com/okonet/lint-staged)
- 在开发和构建中进行代码规范校验
  - [awesome-vite#plugins](https://github.com/vitejs/awesome-vite#plugins) || [vite-plugin-eslint](https://github.com/gxmari007/vite-plugin-eslint)
    - 关闭ESLint的cache，避免因为[缓存问题报错](https://blog.csdn.net/xuefeng11111/article/details/121688821)
- commit message
  > 格式化提交信息，让每一次代码提交都具有实际意义
  - [commitlint](https://github.com/conventional-changelog/commitlint)
    - feat: 新功能
    - fix: 修补bug
    - docs: 文档
    - style: 格式(不影响代码运行的变动)
    - refactor: 重构(既不是新增功能,也不是修改bug的代码变动)
    - test: 增加测试
    - chore: 构建过程或辅助工具的变动
- 在 Vite 中提供 jsx/tsx 支持：[@vitejs/plugin-vue-jsx](https://github.com/vitejs/vite/tree/main/packages/plugin-vue-jsx)
  > 编辑器中的 ESLint 需要配置 "eslint.validate": ["typescriptreact"] 才能验证和格式化 .tsx 文件
  - Vue 中的 JSX 语法：[Babel Plugin JSX for Vue 3.0](https://github.com/vuejs/babel-plugin-jsx)
- [CSS](https://cn.vitejs.dev/guide/features.html#css)
  > 为每一款预处理器内置了特定的Vite插件，但需要安装相应的预处理器依赖
  >为了能够在组件内直接使用全局变量、mixin 等，需要特殊配置,具体配置参见 Vite 官方文档：[css.preprocessorOptions](https://cn.vitejs.dev/config/#css-preprocessoroptions)。
- 该vue3项目单页面组件使用组合式api语法糖的形式编写
- [`<script setup>`内部集成的编译器宏会被eslint报错](https://www.cfanz.cn/resource/detail/WqNljBGlDjjrV)，需做修改，
- 初始化Vue Router && Vuex,配置参照官网
  - `npm install vue-router@4`
  - `npm install vuex@next --save`
- [配置模块路径别名](https://juejin.cn/post/6968327734766338055)
- 和服务端交互基于 [axios](https://github.com/axios/axios) 二次封装，并处理: 接口类型、[多环境baseURL](https://cn.vitejs.dev/guide/env-and-mode.html)、跨域处理([CORS](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/CORS)||[服务器代理](https://cn.vitejs.dev/config/#server-proxy)])、数据mock
- [图标](https://github.com/07akioni/xicons/blob/main/README.zh-CN.md)
- [element-plus](https://element-plus.gitee.io/zh-CN/)安装配置
- layout布局-菜单导航
  - 配置页面路由导航
  - 切换侧边栏展开收起
  - 面包屑导航
- [全屏切换](https://developer.mozilla.org/zh-CN/docs/Web/API/Fullscreen_API)
- [页面加载进度条](https://github.com/rstacruz/nprogress)
