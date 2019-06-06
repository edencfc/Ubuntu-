


> Written with [StackEdit](https://stackedit.io/).
> [Stackedit项目地址](https://github.com/benweet/stackedit.git)
# 项目部署常见问题与解决
## CSS Loader版本匹配
该项目代码在高版本的CSS Loader中会出现报错，最快的处理方法有两种
1. CSS Loader版本降级至0.28
2. 注释掉cssLoader的minimize配置，在该项目中，在utlis.js文件中
```javascript
  var cssLoader = {  
    loader: 'css-loader',  
  options: {  
  // 注释掉，否则编译会报错  
  // minimize: process.env.NODE_ENV === 'production',  
  sourceMap: options.sourceMap  
  }  
  }  
```
## Node Sass could not find a binding for your current environment问题
该问题主要是编译环境的问题，Node.js版本和操作系统切换都会导致报错，如：如果之前是在Windows中编译的，再到Linux中启动就会报错。解决办法
```bash
npm rebuild node-sass
```
## 项目部署
处理完上面两个问题，项目就能正常部署了，参考官方文档
```bash
    # install dependencies
    npm install
    
    # serve with hot reload at localhost:8080
    npm start
    
    # build for production with minification
    npm run build
    
    # build for production and view the bundle analyzer report
    npm run build --report
```
# 在线写Markdown文档并实时同步到Github
进入[StackEdit官网](https://stackedit.io/)，在Workspace中选择Github并授权，就能在线写Markdown并同步了
![file](https://raw.githubusercontent.com/edencfc/Ubuntu-Study/master/img/20-46-59.png)
如果是gitee的话，url的地方输入gitee的地址即可。相对来说，一个比较大的缺点是不能直接上传截图

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg5MDkzOTc5MSwtMjk5MTI3NzE2XX0=
-->