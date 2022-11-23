---
sidebar_position: 1
---

# 前言

该文档将教会你如何使用 `data-collect-template`。

该框架是实现以插件、主题驱动的信息采集的高定制模板。

可应对不同场景的数据手机、信息反馈功能。

框架提供角色管理、权限配置、数据表管理、插件功能、媒体数据保存等功能，使开发者能够注重业务逻辑。

同时后端提供低代码API开发，前端开发者无需了解后端代码知识便可以实现增删查改的功能。

例如：数据收集、官网展示、个人博客、商城、新闻资讯、论坛

# 开发环境

* node版本: `14.18.0`
* php版本: `8.1.10`

# 组件库

本项目默认使用 `Ant Design: 4.24.1`。

# 使用说明

请使用 `npm run load` 命令来安装依赖，这个命令可以将所有主题、插件的依赖一起安装

> 注意，如果你安装新的主题、插件时，无法运行，也请运行这个命令安装依赖

安装程序默认使用 `yarn` 进行安装 （已实现自动判断是否使用pnpm/yarn/npm）

然后使用 `npm run dev` 运行开发环境项目

# 提交规则

该项目默认使用`commitlint`，请遵循该项目规则编写提交内容。

> https://github.com/conventional-changelog/commitlint

# 主题与插件的区别

其实也就是主题主要用于用户访问项目的页面，插件是可以修改模板本身的内容

## 主题

* 提供给用户使用的界面
* 由多个组件、路由构成
* 不能修改模板本身的组件、页面
* 动态加载（首次加载界面需要请求服务器）
* 配置信息中可以写入必有的插件，如果没有装对应的插件，那么将无法使用该主题
* 主题应该有对应的配置提供给后台使用

## 插件

* 由多个动作（action）构成
* 可以修改覆盖模板本身的组件、页面
* 打包项目就已经将插件加载（无需加载，所以可以覆盖原始模板）
* 使用 action 可以在初始化程序时调用

# 公开版、定制版区别

## 路径

### 公开版

* `官网`: www.data-collect.com
* `后台`: www.data-collect.com/admin
* `项目首页`: www.data-collect.com/p/project
* `项目页面`: www.data-collect.com/p/project/page

### 定制版

无法创建多项目，但可以依靠框架使用角色管理、权限配置、数据表管理、插件功能、媒体数据。

* `项目首页`: www.data-collect.com
* `后台`: www.data-collect.com/admin
* `项目页面`: www.data-collect.com/page

# 常见问题

## husky没有生效

* 挂钩未运行
* 确保您的文件名中没有拼写错误。例如，precommit或者pre-commit.sh是无效的名称。有关有效名称，请参阅 Git 挂钩文档。
* 检查git config core.hooksPath返回.husky（或您的自定义挂钩目录）。
* 验证挂钩文件是否可执行。这是在使用husky add命令时自动设置的，但您可以运行`chmod +x .husky/<hookname>`来修复它。
* 检查您的 Git 版本是否大于2.9.

## 如果你的git无法识别文件名大小写修改识别

请使用 `git config core.ignorecase false`
