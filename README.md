[目录]

<!-- TOC -->

- [Zoomla!逐浪CMS卓越出品](#zoomla逐浪cms卓越出品)
    - [Zoomla!Cli-Studio基于VueJS精品全站项目2号站：律师门户整站资源](#zoomlacli-studio基于vuejs精品全站项目2号站律师门户整站资源)
    - [本项目介绍](#本项目介绍)
    - [使用说明](#使用说明)
    - [排错表](#排错表)
- [接口文档](#接口文档)
- [系统运行效果图](#系统运行效果图)

<!-- /TOC -->


# Zoomla!逐浪CMS卓越出品

## Zoomla!Cli-Studio基于VueJS精品全站项目2号站：律师门户整站资源

Zoomla!逐浪CMS：中文业界alexa排名第一的CMS系统|专注.net与windows平台企业级研发，集成内容管理、webfont、商城、店铺、黄页、教育、考试、3D、三维全景、混合现实、CRM、ERP、OA、论坛、贴吧等为一体，打造国内高端的CMS产品典范。

官网：www.z01.com

免费下载：www.z01.com/mb

视频教程：www.z01.com/mtv

模板资源：www.z01.com/mb


QQ交流群号：
[![加入QQ群](https://img.shields.io/badge/一群-541450128-blue.svg?style=for-the-badge&logo=appveyor)](https://jq.qq.com/?_wv=1027&k=5Ephzpq)   [![加入QQ群](https://img.shields.io/badge/二群-601781959-blue.svg?style=for-the-badge&logo=appveyor)](https://jq.qq.com/?_wv=1027&k=50a28BK) 


官方QQ客服：
[![官方QQ客服1](https://img.shields.io/badge/官方QQ客服1-524979923-red.svg?style=for-the-badge&logo=appveyor)](http://wpa.qq.com/msgrd?v=3&uin=745151353&site=qq&menu=yes)  [![官方QQ客服2](https://img.shields.io/badge/官方QQ客服2-1799661890-red.svg?style=for-the-badge&logo=appveyor)](http://wpa.qq.com/msgrd?v=3&uin=1799661890&site=qq&menu=yes) 

## 本项目介绍

这是一个为高端律师事务所构建的全站系统，移动优先，全面支持响应式，其特征包括：
- 服务端基于Zoomla!逐浪CMS v8.1.3数据接口，使用手册http://help.z01.com
- 前端CLI开发框架基于Vue Cli，版本：@vue/cli 4.1.2
- 前端web呈现基于Boostrap V4.x，采用BootstrapVue插件，中文官网http://code.z01.com/bootstrap-vue
- icon图标库基于国产zico图标库，官网http://ico.z01.com
- map地图组件基于vue-baidu-map
- 基于vue-meta组件，完美支持各个页面标题、关键字、网页描述（mkt)描述与SEO|SMO优化
- 支持chrome和现代化浏览器，兼容IE11与EDGE浏览器
- 完美支持微信与小程序接入与二次开发

## 使用说明
1、先安装Vue CLI，安装方法：
```
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```

2、安装nodeJS，即`npm`支持，或`yarn`。

3、获取本程序包后，在程序根目录安装Node环境，安装命令：
```
npm install
# or
yarn install
```

4、运行，输入下面命令就能成功运行：
```
npm run serve
# or
yarn serve
```

5、发布最终版本（最终发布目录存于dist目录下）
```
npm run build
# or
yarn build
```

6、整理和修复文件
```
npm i line
# or
yarn lint
```

## 排错表

**运行时报错：Cannot find module 'webpack/lib/RequestShortener'**
这可能是本地webpack版本问题，建议你执行下面命令纠正它，然后再次运行`npm run serve`：
```npm install webpack --save-dev```

**提示'vue-baidu-map in ./src/main.js'错误，执行安装百度地图组件**
```npm install --save vue-baidu-map```
>安装地图组件时如果出错，请将根目录的`package-lock.json`删除再执行安装，安装完成再恢复`package-lock.json`文件，即可。

**其它几个组件安装方法（如果不报错可忽略并不需要逐一手动安装）**
```
npm install zico
npm install vue bootstrap-vue bootstrap
npm install vue-meta -s
```

# 接口文档
-- [ZoomlaCLI-Studio接口使用说明](源码与接口使用说明/ZoomlaCLI-Studio接口使用说明.md)
-- 本程序目录结构

# 系统运行效果图
![系统效果图1](发布运行效果图/01.jpg)
![系统效果图2](发布运行效果图/02.jpg)
![系统效果图3](发布运行效果图/03.jpg)
![系统效果图4](发布运行效果图/04.jpg)
![系统效果图5](发布运行效果图/05.jpg)
![系统效果图6](发布运行效果图/06.jpg)
![系统效果图7](发布运行效果图/07.jpg)
![系统效果图8](发布运行效果图/08.jpg)
![系统效果图9](发布运行效果图/09.jpg)
![系统效果图10](发布运行效果图/10.jpg)