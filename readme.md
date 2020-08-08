# 登陆
npm login
# 自动更新版本号
npm version patch  // 1.0.1 表示小的bug修复
npm version minor // 1.1.0 表示新增一些小功能
npm version mmajor // 2.0.0 表示大的版本或大升级
npm version preminor // 1.1.0-0 后面多了个0，表示预发布

# 发布
npm publish

# 撤销
npm unpublish packageName --force

# scripts in NPM
- prepare
会在打包和发布包之前以及本地npm install时运行。

- prepublishOnly
在prepare script运行之前运行，并且仅在npm publish运行。
可以运行npm run test & npm run lint以确保不会发布错误的不规范的代码。

- preversion
在发布新版本包之前运行，为了更加确保新版本包的代码规范。npm run lint

- version
在发布新版本包之后运行。如果您的包有关联远程git仓库，每次发布新版本时都会生成一个提交和一个新的版本标记。
那么就可以在此规范代码的命令。

- postversion
在发布新版本包之后运行，在git commit 之后运行，适合推送。