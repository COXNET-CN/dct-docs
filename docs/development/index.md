# 框架开发手册

因为`DCT`本身未开源，该文档是为维护人员及需要二次开发的开发者提供。

# 开发环境

* node版本: `14.18.0`
* php版本: `8.1.10`

# 组件库

本项目默认使用 `Ant Design: 4.24.1`。

# 启动服务

请使用 `npm run load` 命令来安装依赖，这个命令可以将所有主题、插件的依赖一起安装

> 注意，如果你安装新的主题、插件时，无法运行，也请运行这个命令安装依赖

安装程序默认使用 `yarn` 进行安装 （已实现自动判断是否使用pnpm/yarn/npm）

然后使用 `npm run dev` 运行开发环境项目

# 提交规则

该项目默认使用`commitlint`，请遵循该项目规则编写提交内容。

> https://github.com/conventional-changelog/commitlint