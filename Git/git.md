# Git Operations

## Git Commit Example

Below is an example of a git commit.

| Abbreviation | Emoji           | Description                   | Example                                                      |
| ------------ | --------------- | ----------------------------- | ------------------------------------------------------------ |
| bugfix       | 🦠:bug:🦂         | Bugfix<br />错误              | 🦠:bug:🦂`bugfix ➡️ [<go>] <Fix issue with user login.>         |
| doc          | 📔:books:        | Document<br />新增文件        | 📔:books: doc ➡️ [<go>] <Update README with installation instructions.> |
| diary        | 📅               | diary<br />日记               | 📅 diary ➡️ [<go>] <Add daily progress notes.>                 |
| feat         | :sparkles:⭐🌟    | New Feature<br />新增功能     | :sparkles:⭐🌟 feat ➡️ [<go>] <Add user profile picture upload.> |
| hotfix       | :ambulance:🏥    | Hotfix<br />快速修正          | :ambulance:🏥 hotfix ➡️ [<go>] <Quickly resolve critical security issue.> |
| init         | :tada:          | Initialize<br />初始化        | :tada: init ➡️ [<go>] <Initial commit.>                       |
| maintenance  | 🔩:gear:🏭        | Maintenance<br />维謢         | 🔩:gear:🏭 maintenance ➡️ [<go>] <Update project dependencies.> |
| optimize     | :rocket:🛰️       | Optimize<br />优化性能        | :rocket:🛰️ optimize ➡️ [<go>] <Optimize database queries.>     |
| progress     | :construction:🏗️ | In Progress<br />协作中       | :construction:🏗️ progress ➡️ [<go>] <Work in progress on user registration feature.> |
| refactor     | :hammer:⚒️🛠️      | Refactor<br />重构            | :hammer:⚒️🛠️ refactor ➡️ [<go>] <Refactoring database connection handling.> |
| remove       | :fire:          | Remove<br />移除              | :fire: remove ➡️ [<go>] <Remove obsolete function.>           |
| style        | :art:🖼️          | Style<br />更改风格           | :art:🖼️ style ➡️ [<go>] <Format code according to style guide.> |
| test         | 🧪🧫⚗️             | Test<br />测试                | 🧪🧫⚗️ test ➡️ [<go>] <Add unit tests for authentication service.> |
| test-related | 🩺:microscope:🩻  | Test-related<br />测试相关    | 🩺:microscope:🩻 test-related ➡️ [<go>] <Write integration tests for API.> |
| update-doc   | :scroll:🗞️       | Update Document<br />更新文件 | :scroll:🗞️ update-doc ➡️ [<go>] <Update API documentation for v2.0.> |

Write the template to the file.

```bash
$ cat << EOF > ~/.gitmessage.txt
# The following are examples. 以下为范例
# 🦠🐛🦂 bugfix ➡️ [<go>] <Fix issue with user login.> 错误
# 📔📚 doc ➡️ [<go>] <Update README with installation instructions.> 新增文件
# 📅 diary ➡️ [<go>] <Add daily progress notes.>
# ✨⭐🌟 feat ➡️ [<go>] <Add user profile picture upload.> 新增功能
# 🚑🏥 hotfix ➡️ [<go>] <Quickly resolve critical security issue.> 快速修正
# 🎉 init ➡️ [<go>] <Initial commit.> 初始化
# 🔩⚙️🏭 maintenance ➡️ [<go>] <Update project dependencies.> 维謢
# 🚀🛰️ optimize ➡️ [<go>] <Optimize database queries.> 优化性能
# 🚧🏗️ progress ➡️ [<go>] <Work in progress on user registration feature.> 协作中
# 🔨⚒️🛠️ refactor ➡️ [<go>] <Refactoring database connection handling.> 重构
# 🔥 remove ➡️ [<go>] <Remove obsolete function.> 移除
# 🎨🖼️ style ➡️ [<go>] <Format code according to style guide.> 更改风格
# 🧪🧫⚗️ test ➡️ [<go>] <Add unit tests for authentication service.> 测试
# 🩺🔬🩻 test-related ➡️ [<go>] <Write integration tests for API.> 测试相关
# 📜🗞️ update-doc ➡️ [<go>] <Update API documentation for v2.0.> 更新文件
# 
# 🔴 Set up the project with basic files and configurations.
# 🔴 Resolved a bug that prevented users from logging in.
# 🔴 Remove obsolete function.
EOF
```

Write the template to the Git configuration.

````bash
$ git config --global commit.template ~/.gitmessage.txt
````

## Reduce the size of the Git repository

Cleanup unnecessary files and optimize the local repository.

```bash
git gc --aggressive --prune=all
```

Clear operation logs.

```bash
git reflog expire --expire=now --all
git gc --prune=now
```

Optimize pack files.

```bash
git repack -Ad
```



