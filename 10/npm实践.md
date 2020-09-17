
# 发布npm包-publish npm
```bash
mkdir qingcheng
npm init 
npm login
npm publish --access=public
```

您首先执行下 npm adduser ，输入您相应的 Username 、 Password 、 Email: (this IS public) ，关键的一步来了!

Logged in as 您的Username on https://registry.npmjs.org/.
如果 on 后面不是 https://registry.npmjs.org/ ，而是其他的镜像，比如我们大家常见的淘宝镜像：

http://registry.npm.taobao.org/
那么您首先替换成原来的，替换成原来执行如下命令：

npm config set registry https://registry.npmjs.org/
最后，替换完毕再执行 npm adduser 、 npm publish ，这样应该就ok了！