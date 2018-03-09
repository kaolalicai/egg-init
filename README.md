klg-init
=======
copy from egg-init

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
? Please select a boilerplate type (Use arrow keys)
❯ module - npm module
  project - klg project use koa(todo)
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

## License

[MIT](LICENSE)
