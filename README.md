# Vue 3 + Typescript + Vite

This template should help get you started developing with Vue 3 and Typescript in Vite.

随记：

- 项目采用[vite](https://cn.vitejs.dev/)来进行构建打包
  - vite并没有集成eslint，需要自行[添加](https://eslint.org/docs/user-guide/getting-started)
  - 手动配置eslint验证规则以此来适配vue3
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
