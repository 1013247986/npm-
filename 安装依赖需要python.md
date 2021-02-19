#### 1、npm i 的时候，需要安装python

````js
// 报错内容 
// Can't find Python executable "python" , you can set the PYTHON env variable

// 第一步：安装python
npm i --global --prodouction windows-build-tools
// 第二步：用到sass的再安装sass
npm i node-sass --save-dev

// 注：如果没有网络，可以用python 包离线安装环境，python包要2.7版本的，3以上的没有用
// 离线安装后需要在电脑属性，高级系统设置，环境变量里面配置 系统变量
````

**需要python的原因：**

 node-sass有些模块是用python为底层写的，所以需要python环境，但是现在也有纯js的包，不依赖python环境

**没有网络安装python后1**

```js
// 安装 npm i node-sass 会报错，其中win32-x64-64_binding.node等字样就是我们需要下载的版本，版本不同名字有所差别；也可以使用
// 因为没有网络，他下载不了，通过有网络的电脑下载在git上下载好，然后随便放一个地方，然后配置环境变量
// 1、在用户变里配置SASS_BINARY_PATH变量，变量值填入下载文件路径
// 2、在系统变量PATH的变量值中添加下载文件路径
// 3、然后重新npm i ,如果不成功说明环境变量没有生效，重启电脑就好了
```

**没有网络安装python后2**

```js
//到有网络的电脑或者启动过的项目中 到node-moudle下面找到node-sass文件夹直接拷贝，也可以，（亲测可试）

//但是有一个前提，就是你电脑的node版本需要和拷贝node-sass电脑的版本一致，如果不一致，自己自行安装对应的node版本，如果不对可能会报错
```