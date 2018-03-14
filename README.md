klg-init
=======
fork [egg-init](https://github.com/eggjs/egg-init)

Kalengo 内部项目初始化工具。
可以初始化 npm module 和 koa web 项目

## Install

```bash
$ npm i klg-init -g
$ klg-init -h
```

## 创建 `module` 类型的应用

```bash
$ klg-init --type module [dest]
```

## 不输入类型可以选择

```bash
$ klg-init dest
[klg-init] fetching npm info of klg-init-config
? Please select a boilerplate type (Use arrow keys)
  ──────────────
❯ module - npm 库项目模板 
  model - mongoose model 模板 todo 
  project - JavaScript 后端项目模板 todo 
  project-ts - Typescript 后端项目模板 todo 
  admin - 管理后台项目模板 todo 

```

## 支持的参数

```
Usage: klg-init [dir] --type=module

Options:
  --type          boilerplate type                                                [string]
  --dir           target directory                                                [string]
  --force, -f     force to override directory                                     [boolean]
  --package       boilerplate package name                                        [string]
  --registry, -r  npm registry, support china/npm/custom, default to auto detect  [string]
  --silent        don't ask, just use default value                               [boolean]
  --version       Show version number                                             [boolean]
  -h, --help      Show help                                                       [boolean]
```

## 自定义模板

自定义模板采用 npm 包的形式管理

- 新建仓库如 [klg-boilerplate-module](https://github.com/kaolalicai/klg-boilerplate-module)
- boilerplate 目录下存放所有的初始化文件
- 可以使用 `klg-init --template=PATH` 本地检查生成效果
- index.js 文件可以声明要替换的变量，在 boilerplate 文件夹中写模板的时候，可以通过 `{{name}}` 占位符的方式进行替换

```js
module.exports = {
  name: {
    desc: '插件名',
  },
  description: {
    desc: '插件描述',
  },
  author: {
    desc: '作者',
  },
};
```

- 更新依赖关系，只需要指定你的包名，更新到 [klg-init-config](https://github.com/kaolalicai/klg-init-config) 这个模块的 package.json 中 `config.boilerplate` 字段
- 发布模板（和配置）到 npm

## License

[MIT](LICENSE)
