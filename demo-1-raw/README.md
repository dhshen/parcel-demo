#demo-1
```
yarn init -y
```
新建index.html
```$xslt
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>demo-1</title>
</head>
<body>
    DEMO页
    <script src="./index.js"></script>
</body>
</html>
```
新建index.js
```$xslt
console.log('hello,parcel')
```
命令行敲入：
```$xslt
F:\myspace\parcel-demo\demo-1>parcel index.html
Server running at http://localhost:1234
✨  Built in 794ms.
```
在浏览器中访问http://localhost:1234可以跑起应用
再在index.js中随便添加一个打印并保存，可以看到应用热更新