# 1. webpack 介绍
## 相关网址
# 2. webpack 基础
##  2.1. webpack环境安装
⚠️注意：先全局安装，再局部安装，老是提示安装webpack-cli，把全局的webpack、webpack-cli卸载后重装 重启
```bash
先全局安装webpack和webpack-cli
npm install webpack -g
npm install webpack-cli -g
再局部安装webpack和webpack-cli
npm install webpack --save-dev
npm install webpack-cli --save-dev
```
## 2.2. webpack-cli 的使用

## 2.3. npx 的原理介绍

## 2.4. webpack 的应用场景

## 2.5. webpack 的集成配置

## 2.6. 将 webpack 命令配置到 package.json

## 2.7. watch 模式

## 2.8. webpack-dev-server 的基本使用

## 2.9. html插件-html-webpack-plugin的使用

## 2.10. webpack-dev-middleware 的基本使用

## 2.11. 自动编译工具总结

## 2.12. loader 处理 css 文件

## 2.13. loader-处理 less 和 sass 文件

## 2.14. loader-处理图片和字体文件

## 2.15. loader-自定义图片打包目录和打包名称

## 2.16. loader-处理 js 文件之 babel 的基本使用

## 2.17. loader-处理js文件之转换更高级的用法

## 2.18. loader-处理js文件之转行generator的语法

## 2.19. loader-处理js文件之使用.babelrc配置文件

## 2.20. loader-处理js文件之高版本的原型方法转义

## 2.21. source map的使用

## 2.22. 插件-clean-webpack-plugin


## 2.23. 插件-copy-webpack-plugin

## 2.24. 插件-BannerPlugin


# 3. webpack 高级
## 3.1. HTML中img标签的图片资源处理

## 3.2. 多页应用打包

## 3.3. 第三方库的两种引入方式

## 3.4. 区分环境配置文件打包

## 3.5. 区分环境配置文件打包-配置文件归类

## 3.6. 定义环境变量区分开发环境与生产环境

## 3.7. 跨域问题简介及常用的解决方案

## 3.8. 使用http-proxy解决跨域问题

## 3.9. HMR的使用
# 4. webpack 优化

## 4.1. production模式打包自带优化
## 4.2. production 模式打包自带优化-scope-hoisting

## 4.3. css优化-将css提取到独立的文件中

## 4.4. css优化-自动添加css前缀

## 4.5. css优化-开启css压缩

## 4.6. js代码分离-CodeSplitting简介

## 4.7. js代码分离-手动配置多入口实现代码分割

## 4.8. js代码分离-多入口打包抽取公共代码

## 4.9. js代码分离-动态导入的基本使用
## 4.10. js代码分离-静态导入的问题

## 4.11. js代码分离-动态导入的好处


## 4.12. SplitChunksPlugin 的配置参数-chunks

## 4.13. SpliteChunksPlugin的配置参数-通用配置

## 4.14. SplitChunksPlugin的配置参数-cacheGroups

## 4.15. 提高构建性能-noParse

## 4.16. 提高构建性能-IgnorePlugin简介

## 4.17. 提高构建性能-moment简介


## 4.18. 提高构建性能-IgnorePlugin的使用


## 4.19. 提高构建性能-使用noParse的注意事项

## 4.20. 提高构建性能-DllPlugin简介

## 4.21. 提高构建性能-Vue环境部署及问题说明


## 4.22. 提高构建性能-使用DllPlugin打包Vue全家桶

## 4.23. 提高构建性能-使用DllReferencePlugin关联Dll库

## 4.24. 提高构建性能-使用add-asset-webpack-plugin自动添加js引用

# 5. 常见问题