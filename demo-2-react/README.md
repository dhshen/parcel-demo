#demo-2
本demo参考自：[前端外刊评论-Parcel，零配置开发 React 应用！](https://zhuanlan.zhihu.com/p/32375500)

##步骤
首先，创建一个 NPM 项目：
```$xslt
mkdir demo-2
cd demo-2
npm init -y
```


下一步安装 React、babel 和 Parcel 依赖：
```$xslt
npm install --save react
npm install --save react-dom
npm install --save-dev babel-preset-react
npm install --save-dev babel-preset-env
npm install --save-dev parcel-bundler 
```
或
```$xslt
yarn add react react-dom
yarn add --dev babel-preset-react babel-preset-env parcel-bundler
```

接下来，创建 .babelrc 文件，告诉 parcel 我们使用 ES6 和 React JSX：
```$xslt
{
  "presets": ["env", "react"]
}
```
创建 React App，就两个文件：
index.html：
```$xslt
<!DOCTYPE html>
<html>
    <head>
        <title>React starter app</title>
    </head>
    <body>
        <div id="app"></div>
        <script src="index.js"></script>
    </body>
</html>
```
index.js：
```$xslt
import React from "react";
import ReactDOM from "react-dom";

class HelloMessage extends React.Component {
  render() {
    return <div>Hello {this.props.name}</div>;
  }
}

var mountNode = document.getElementById("app");
ReactDOM.render(<HelloMessage name="Jane" />, mountNode);
```
现在，只需要在 package.json 添加一个启动脚本就可以把我们的应用跑起来了：
```$xslt
"scripts": {
  "start": "parcel src/index.html",
}, 
```
搞定，启动：
```$xslt
npm start
```
