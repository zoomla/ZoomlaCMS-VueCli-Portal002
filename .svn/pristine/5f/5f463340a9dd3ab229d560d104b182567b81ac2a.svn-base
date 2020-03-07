[目录]
<!-- TOC -->

- [ZoomlaCLI-Studio接口使用说明](#zoomlacli-studio%e6%8e%a5%e5%8f%a3%e4%bd%bf%e7%94%a8%e8%af%b4%e6%98%8e)
  - [版本信息](#%e7%89%88%e6%9c%ac%e4%bf%a1%e6%81%af)
  - [文档结构说明](#%e6%96%87%e6%a1%a3%e7%bb%93%e6%9e%84%e8%af%b4%e6%98%8e)
  - [ZoomlaCLI-Studio中的models接口配置项说明](#zoomlacli-studio%e4%b8%ad%e7%9a%84models%e6%8e%a5%e5%8f%a3%e9%85%8d%e7%bd%ae%e9%a1%b9%e8%af%b4%e6%98%8e)
    - [配置文件](#%e9%85%8d%e7%bd%ae%e6%96%87%e4%bb%b6)
    - [接口信息](#%e6%8e%a5%e5%8f%a3%e4%bf%a1%e6%81%af)
    - [接口用例](#%e6%8e%a5%e5%8f%a3%e7%94%a8%e4%be%8b)
  - [Zoomla!CLI-Studio之远程服务端配置](#zoomlacli-studio%e4%b9%8b%e8%bf%9c%e7%a8%8b%e6%9c%8d%e5%8a%a1%e7%ab%af%e9%85%8d%e7%bd%ae)
    - [第一步：启用远程JSONP接口](#%e7%ac%ac%e4%b8%80%e6%ad%a5%e5%90%af%e7%94%a8%e8%bf%9c%e7%a8%8bjsonp%e6%8e%a5%e5%8f%a3)
    - [第二步：配置appid和apikey项](#%e7%ac%ac%e4%ba%8c%e6%ad%a5%e9%85%8d%e7%bd%aeappid%e5%92%8capikey%e9%a1%b9)
  - [扩展资源](#%e6%89%a9%e5%b1%95%e8%b5%84%e6%ba%90)
    - [sass/scss官方手册](#sassscss%e5%ae%98%e6%96%b9%e6%89%8b%e5%86%8c)
    - [Boostrap 中国站](#boostrap-%e4%b8%ad%e5%9b%bd%e7%ab%99)
    - [zico图标库](#zico%e5%9b%be%e6%a0%87%e5%ba%93)
    - [Uni全球字码表](#uni%e5%85%a8%e7%90%83%e5%ad%97%e7%a0%81%e8%a1%a8)
    - [webfont字体引用](#webfont%e5%ad%97%e4%bd%93%e5%bc%95%e7%94%a8)

<!-- /TOC -->


# ZoomlaCLI-Studio接口使用说明
## 版本信息
接口版主程序版本：v8.1.3
匹配逐浪CMS版本：V8.1.3

## 文档结构说明
    |-- dis             //目录编译输出
    |-- src             //主要开发目录
    |   |-- App.vue
    |   |-- main.js
    |   |-- assets      //资源目录，放自定义开发资源
    |       |-- images  //自定义图片资源，项目build后会加上md5字符串编译
    |       |-- global.scss  //全局CSS，逐浪CMS卓越前端不采用分散CSS编译
    |       |-- _zoomlaCMS.scss  //逐浪SCSS之mixin混合文件
    |   |-- assets
    |   |-- components  //组件目录，带全局组件，本案中如ZoomlaFoot.vue、ZoomlaKefu.vue、Zoomla_plus_iteam.vue均代表不同的组件
    |   |-- models      //与远程jsonp接口配置项
    |   |-- plugins     //扩展插件
    |   |-- router      //路由定义，相当于栏目节点定义
    |   |-- views       //页面配置，相当于节点/频道/内容模板
    |   |-- App.vue     //全局vue文件，相当于全站模板
    |   |-- main.js     //全局组件插件配置，相当于逐浪CMS的全局配置。

## ZoomlaCLI-Studio中的models接口配置项说明
>此处于配置接口，用于实现与远程服务端的内容交互（如果您不需要支持访客留言、内容更新，则可以忽略这一段，当然我们推荐使用此配置项，从而使站点拥有强大的功能）。

### 配置文件
models目录位于`/src/models`位置。
下面有三个文件：
- common.js
- HTTP.js
- Regex.js

远程jsonp接口配置文件主要在`common.js`
打开`common.js`文件，在第16行位置，可以看到如下信息：
```
const baseUrl = 'http://网址/API/WXAPP?apiId=eecabae94e760d1c50157f35b5d4aa72&apiKey=c13b007c8feb97803c24f76735a820b2&action=';
		let url = baseUrl+action;
```
### 接口信息
从上面可以看到，一个完整的接口包括以下三个部份信息：
- url信息，即上面的“网址”字段，这是你的服务端网址
- appid，这需要您的Zoomla!逐浪CMS后台分配
- apikey，这需要您的Zoomla!逐浪CMS后台分配

### 接口用例
从上面接口中，我们可以加不同的调式用例，实现不同的远程信息调用：
```
# 模型列表
http://网址/API/WXAPP?apiId=eecabae94e760d1c50157f35b5d4aa72&apiKey=c13b007c8feb97803c24f76735a820b2&action=model_list  

# 节点列表
http://网址/API/WXAPP?apiId=eecabae94e760d1c50157f35b5d4aa72&apiKey=c13b007c8feb97803c24f76735a820b2&action=node_list  

# 父节点下多节点列表
http://网址/API/WXAPP?apiId=eecabae94e760d1c50157f35b5d4aa72&apiKey=c13b007c8feb97803c24f76735a820b2&action=node_list&pid=1

# 内容读取
http://网址/API/WXAPP?apiId=eecabae94e760d1c50157f35b5d4aa72&apiKey=c13b007c8feb97803c24f76735a820b2&action=content_list&pnid=[节点ID]
```
**注以上文档中的appid和apikey均为临时信息，不同站点配置信息不同，需要自定义配置 。**

## Zoomla!CLI-Studio之远程服务端配置 
为增强安全，Zoomla!逐浪CMS远程JSONP接口并非默认开通，需要站长根据需求，手动开通，并配置相关信息，才可以使用。

### 第一步：启用远程JSONP接口
![01-开启接口](01-开启接口.jpg) 

### 第二步：配置appid和apikey项
![02-获取appid和apikey](02-获取appid和apikey.jpg) 

> 注：Zoomla!逐浪CMS每个分行版本，可能接口和UI会有改进和调整，相关信息敬请访问www.z01.com官网，或通过下面方法获得服务：

官网：www.z01.com
帮助中心： http://help.z01.com
快手抖音B站和youtube搜索：最帅程序员发哥



QQ交流群号：
[![加入QQ群](https://img.shields.io/badge/一群-541450128-blue.svg?style=for-the-badge&logo=appveyor)](https://jq.qq.com/?_wv=1027&k=5Ephzpq)   [![加入QQ群](https://img.shields.io/badge/二群-601781959-blue.svg?style=for-the-badge&logo=appveyor)](https://jq.qq.com/?_wv=1027&k=50a28BK) 


官方QQ客服：
[![官方QQ客服1](https://img.shields.io/badge/官方QQ客服1-524979923-red.svg?style=for-the-badge&logo=appveyor)](http://wpa.qq.com/msgrd?v=3&uin=745151353&site=qq&menu=yes)  [![官方QQ客服2](https://img.shields.io/badge/官方QQ客服2-1799661890-red.svg?style=for-the-badge&logo=appveyor)](http://wpa.qq.com/msgrd?v=3&uin=1799661890&site=qq&menu=yes) 

电话：021-50391046、13177777714


## 扩展资源
### sass/scss官方手册 
sass/scss官方手册 http://code.z01.com/sass
### Boostrap 中国站 
Boostrap 中国站 http://code.z01.com/v4
### zico图标库 
zico图标库 http://ico.z01.com
### Uni全球字码表 
Uni全球字码表 http://www.ziti163.com/uni
### webfont字体引用 
webfont字体引用 http://www.ziti163.com/webfont

