# 常见问题

## husky没有生效

* 挂钩未运行
* 确保您的文件名中没有拼写错误。例如，precommit或者pre-commit.sh是无效的名称。有关有效名称，请参阅 Git 挂钩文档。
* 检查git config core.hooksPath返回.husky（或您的自定义挂钩目录）。
* 验证挂钩文件是否可执行。这是在使用husky add命令时自动设置的，但您可以运行`chmod +x .husky/<hookname>`来修复它。
* 检查您的 Git 版本是否大于2.9.

## 如果你的git无法识别文件名大小写修改识别

请使用 `git config core.ignorecase false`
