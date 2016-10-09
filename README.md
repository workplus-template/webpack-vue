#webpack-vue

>A starter project for using VueJs with Webpack via Babel!

### 技术栈

* VueJs
* Vuex
* Vue-router
* Less
* ES6
* Webpack
* Babel

### 安装

确保已经安装workplus-cli

```bash
$ npm install workplus-cli -g
```

然后执行以下命令：

```bash
$ workplus start webpack-vue my-project
```

安装完成后，进入项目目录，执行`npm install`

### 开发

#### a. 开发模式

```bash
$ npm run dev
```

默认端口为8080，可通过配置package.jso文件的scripts属性来修改端口。

#### b. 设置代理

在webpack.config.js中设置[devServer](http://webpack.github.io/docs/webpack-dev-server.html)，大概配置如下：

```js
var config = {
  ...
  devServer: {
    '/api': {
      target: 'http://api.example.com'
    }
  }
}
```

切记：若使用该代理，访问接口应该为相对路径，既接口为`http://some.example.com/topics`，应写成`/topics`。

#### c. 发布

```bash
$ npm run build
```

代码将会打包到`dist`文件夹，可以使用workplus进入dist文件夹并启动server进行测试。

### Author

[Hejx](https://github.com/Alex-fun)


