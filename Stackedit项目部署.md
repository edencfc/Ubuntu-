


> Written with [StackEdit](https://stackedit.io/).
> [Stackedit项目地址](https://github.com/benweet/stackedit.git)
# CSS Loader版本匹配
该项目代码在高版本的CSS Loader中会出现报错，最快的处理方法有两种
1. CSS Loader版本降级至0.28
2. 注释掉utils.js文件中的minimize配置
```javascript
var cssLoader = {  
  loader: 'css-loader',  
  options: {  
    // minimize: process.env.NODE_ENV === 'production',  
  sourceMap: options.sourceMap  
  }  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQ4NTgyMzA1NV19
-->