# WechatHelper
 
## 宝宝波的专属助手

让你闲置的微信号成为你的日常宝宝波的专属助手（没有闲置的也没关系，添加我的小助手微信号，给你分配一个宝宝波的专属助手）
## 功能

很听你话的私人宝宝波的专属助手，帮你创建定时任务，每日提醒，纪念日提醒，当日提醒

文字支持格式：（关键词之间需要用空格分开，）

* “提醒 我 18:30 快要下班了，准备一下，不要忘记带东西” **（当天指定时间提醒）**
* “提醒 其他人昵称 2019-09-10 10:00 工作再忙，也要记得喝水”**（委托宝宝波的专属助手提醒其他人）**
* “提醒 我 每天 8:00 出门记得带钥匙，公交卡还有饭盒”**（每日指定时间提醒）**
* “提醒 wo 2019-09-10 10:00 还有两天就是女票的生日，要提前准备一下” **（指定日期时间提醒）**


为了让数据持久化，使用了mongodb数据库，保存所有的定时任务，所以需要本地安装好mongodb数据库，本项目mongodb端口默认27017

## 项目运行

由于需要安装chromium,所以要先配置一下镜像，注意由于wechaty的限制，必须使用node10以上版本

### npm或者yarn 配置淘宝源

**(很重要，防止下载chromium失败，因为下载文件在150M左右，所以在执行npm run start后需要等待下载大概一两分钟以上，请耐心等待)**
npm

    npm config set registry https://registry.npm.taobao.org
    npm config set disturl https://npm.taobao.org/dist
    npm config set puppeteer_download_host https://npm.taobao.org/mirrors
yarn

    yarn config set registry https://registry.npm.taobao.org
    yarn config set disturl https://npm.taobao.org/dist
    yarn config set puppeteer_download_host https://npm.taobao.org/mirrors


### 下载项目安装依赖

    git clone git@github.com:gengchen528/wechat-assistant.git
    cd wechat-assistant.git
    npm install
    npm run start
    
### 扫描登录

用微信扫描控制台显示的二维码，在手机上同意登录即可。使用其他微信发送指定格式文字进行添加定时任务。

## 服务器部署
1、如果需要在服务器中部署，需要先扫描二维码登录一次，生成微信维持登录状态的json文件

2、生成此文件后，可以使用pm2工具进行进程守护。由于为了方便，本地开发的时候，我设置的`npm run start`同时执行了两条命令，所以在服务器端部署的时候，建议先启动`koa.js`后再启动`index.js`
## 注意

 本项目属于个人兴趣开发，开源出来是为了技术交流，请勿使用此项目做违反微信规定或者其他违法事情。
 建议使用小号进行测试，有被微信封禁网页端登录权限的风险（客户端不受影响），请确保自愿使用。
 
