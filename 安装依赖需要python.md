#### 1、npm i 的时候，需要安装python

````js
// 报错内容 
// Can't find Python executable "python" , you can set the PYTHON env variable

// 第一步：安装python
npm i --global --prodouction windows-build-tools
// 第二步：用到sass的再安装sass
npm i node-sass --save-dev

// 注：如果没有网络，可以用python 包离线安装环境，python包要2.7版本的，3以上的没有用
````

**需要python的原因：**

 node-sass有些模块是用python为底层写的，所以需要python环境，但是现在也有纯js的包，不依赖python环境