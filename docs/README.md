![1](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105151907.jpeg)

## 写在前面

- 关于封面

  我是中国人，当然要打出我们的大国宝啦。另外这是文明致敬Nodejs的一种方式，搭配程序员都爱的学习网站logo风格，别有一番滋味在心头~

  ![u=3397689449,4160955919&fm=26&gp=0](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105151847.jpeg)

  

- 本地编译：

  Markdown编辑器使用[Typora](https://typora.io/)

  主题使用[Drake](https://theme.typora.io/theme/Drake/)

  

- 联系我：

  微信：

  intereting1366

  邮箱：

  gaofeng_zgf@163.com

  nicolasgaofeng@gmail.com

  

- 声明：

  这是一份自己学习Nodejs从入门到踩坑到跑路的记录。

  如果本仓库存在的内容对您和您的利益产生损害，请立即私信，我们将在最短时间内对其做出处理。

  

- 鸣谢：

  如果文中出现错误，请与我联系。向你敬礼！

## 一、下载及安装

### 1.1 下载

官网下载地址：http://nodejs.cn/download/

根据自己需要下载对应的版本即可,我下载的是windows系统64位的版本。

![1.1.1](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003202.png)

### 1.2 安装

1.2.1 安装第一步直接点Next。

![1.2.1](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003221.png)

1.2.2 把选项打勾之后点击Next。

![1.2.2](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003250.png)

1.2.3 设置安装路径，设置完成之后点击Next。

![1.2.3](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003259.png)

1.2.4 点击Next。

![1.2.4](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003306.png)

1.2.5 点击Install安装。

![1.2.5](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003315.png)

1.2.6 等待安装完成。

![1.2.6](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003321.png)

1.2.7 点击Finish完成安装。

![1.2.7](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003331.png)

1.2.8 查看node.js是否安装成功

windows下打开 cmd 输入以下命令行

```
node -v
npm -v
```

npm 随安装程序自动安装，作用就是对 Node.js 依赖的包进行管理

![1.3](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003348.png)

### 1.3 配置

1.3.1 配置全局目录

因为在执行例如npm install -g等命令全局安装的时候，默认会将模块安装在C:\Users\用户名\AppData\Roaming路径下的npm和npm_cache中，不方便管理且占用C盘空间，所以这里配置自定义的全局模块安装目录

在nodejs目录下，新建node_global、node_cache两个文件夹，然后运行以下2条命令：

```
npm config set prefix "D:\software\nodejs\node_global"
npm config set cache "D:\software\nodejs\node_cache"
```

**注意：**引号里的目录是你自己Node.js的安装地址

查看npm的本地仓库，输入命令

```
npm list -global
```

1.3.2 配置环境变量

在环境变量 -> 系统变量中新建一个变量名为 “NODE_PATH”， 值为“D:\Program Files\nodejs\node_modules”，如下图所示

![1.4.2](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003527.png)

然后编辑用户变量里的Path，将相应npm的路径改为：D:\software\nodejs\node_global，如下：

![1.4.2.2](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003535.png)



1.3.3 配置镜像站

输入命令

```
npm config set registry=http://registry.npm.taobao.org 
```

![1.4.3](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003551.png)

查看镜像站是否有用，看看能否获得vue的信息。如下图所示

```
npm info vue 
```

![1.4.3.2](https://gitee.com/zgf1366/pic_store/raw/master/img/20210105003600.png)

1.3.4 配置完成。