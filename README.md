# 使用说明

本框架是一套基于vant封装的开箱即用的移动端框架，使用本框架不需要再从`vue create project`命令开始了，本框架内部提供了许多配置，只需要进行少量调整即可开始功能开发。

# 功能点

 ### 代码规范

  本框架内部集成了`eslint`与`stylelint`，全方位的去管控代码规范，为了方便使用，建议使用开发工具如 `vscode` 时需要安装`eslint`与`stylelint`插件

  ### 提交规范

  虽然定义了`eslint`和`stylelint`，但是假如在提交代码时不去校验，那么也无法有效的限制，所以定义了提交规范，在提交时会自动校验代码格式，并自动格式化。

  同时，对于提交，也添加了`commitlint`，提交时需要按照固定的格式进行提交，如 `git commit -m 'feat: 增加了一个新的功能'`，具体可参考`commitlint.config.js`文件内的注释

  ### `cdn`
  如果项目需要使用`cdn`的话，经常会将`cdn`的地址添加到`index.html`文件内，同时要对开发和生产环境进行区分，为了方便开发，框架内将`cdn`提取到了固定的文件内`cdn.js`，在这个文件内可以指定哪些文件使用`cdn`，同时有开关可以直接关闭`cdn`,具体文件在 `config/cdn.js`文件中

  ### 工具类

  框架对`axios`进行了二次封装，可以满足大家基本的使用需求，同时也提供了日期工具类，不需要再继续造轮子

  ### `mock`

  我没有使用`mock.js`，在这里作者建议大家使用`yapi` 或 `Doclevel`，框架内有一个目录 `mock`, 在这里可以配置哪些接口走`mock`,哪些不走

  ### 目录结构
   整个框架目录结构比较完整，基本可以满足常规开发，同时，为了提供功能复用，对于组件，分成了`base`与`components`两个目录，`base`里面放没有业务的基本组件,`components`里面放业务相关的组件，同时`base`目录里面提供了一个`loading`组件，在页面使用时可以直接使用`this.$loading()`调用



## 所有命令

使用本框架建议使用`yarn`进行安装启动，安装`yarn`请执行 `npm install yarn -g`

``` 安装
yarn install
```

### 启动
```
yarn serve
```

### 打包
```
yarn build
```

### 代码校验
```
yarn lint
```


我是子君，如果喜欢，请给一个star 谢谢，也可以关注公众号【前端有的玩】一起玩前端



