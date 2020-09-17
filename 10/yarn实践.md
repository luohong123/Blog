yarn add

```javascript
yarn add <packageName> --dev 依赖会记录在 package.json 的 devDependencies 下
```

```javascript
yarn add webpack --dev # yarn 简写 -D
yarn global add <packageName> 全局安装依赖
yarn global add webpack # yarn
```

## 更新

```javascript
yarn upgrade # 升级所有依赖项，不记录在 package.json 中
npm update # npm 可以通过 ‘--save|--save-dev’ 指定升级哪类依赖
yarn upgrade webpack # 升级指定包
npm update webpack --save-dev # npm

yarn upgrade --latest # 忽略版本规则，升级到最新版本，并且更新 package.json
```

## 移除

yarn remove <packageName>
