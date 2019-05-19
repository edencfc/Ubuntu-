


> Written with [StackEdit](https://stackedit.io/).
> [Stackedit项目地址](https://github.com/benweet/stackedit.git)
# CSS Loader版本匹配
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
# Node Sass could not find a binding for your current environment问题
该问题主要是编译环境的问题，Node.js版本和操作系统切换都会导致报错，如：如果之前是在Windows中编译的，再到Linux中启动就会报错。解决办法


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMzczNTY2NzVdfQ==
-->