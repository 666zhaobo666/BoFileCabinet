<div align="center">
<h1>文件快递柜</h1>
</div>

![pCVk67d.png](https://s1.ax1x.com/2023/06/10/pCVk67d.png)

## 简介

- [x] 轻量简洁：Fastapi+Sqlite3+Vue2+ElementUI
- [x] 轻松上传：复制粘贴，拖拽选择
- [x] 多种类型：文本，文件
- [x] 防止爆破：错误次数限制
- [x] 防止滥用：IP限制上传次数
- [x] 口令分享：随机口令，存取文件，自定义次数以及有效期
- [x] 匿名分享：无需注册，无需登录
- [x] 管理面板：查看所有文件，删除文件
- [x] 多种存储方式：阿里云OSS、本地文件流

## 部署方式

### 💁‍♀️ 宝塔部署

#### 1. 安装Python项目管理器

❗️❗️❗️ 注意：必须安装2.0版本，否则必失败

![image.png](https://cdn.nlark.com/yuque/0/2023/png/1328158/1677585822319-d3466029-2181-496d-922a-3323f40706a4.png?x-oss-process=image%2Fresize%2Cw_959%2Climit_0)

![image.png](https://cdn.nlark.com/yuque/0/2023/png/1328158/1677585835397-52ab9813-5beb-49cb-b37b-ac613b4c50db.png?x-oss-process=image%2Fresize%2Cw_711%2Climit_0)

#### 2. 安装Python3.9.10

点击设置->版本管理->Python版本->3.9.10[未安装]->安装版本

![image.png](https://cdn.nlark.com/yuque/0/2023/png/1328158/1677583572094-be526fd9-5965-4e3a-a862-1227a347ed2e.png)

安装完成

![image.png](https://cdn.nlark.com/yuque/0/2023/png/1328158/1677583876694-51253089-c383-4c03-9fc1-429ba377c706.png)

#### 3. 下载源码

GitHub地址：https://github.com/666zhaobo666/BoFileCabinet





回到宝塔，新建一个空白目录`BoFileFabient`

![pCVAcKU.png](https://s1.ax1x.com/2023/06/10/pCVAcKU.png)

进入目录，粘贴远程下载源码

![pCVAfa9.png](https://s1.ax1x.com/2023/06/10/pCVAfa9.png)

解压

![pCVZubF.png](https://s1.ax1x.com/2023/06/10/pCVZubF.png)

打开Python项目管理器->添加项目

![pCVEeGq.png](https://s1.ax1x.com/2023/06/10/pCVEeGq.png)

启动成功！

![pCVEQLF.png](https://s1.ax1x.com/2023/06/10/pCVEQLF.png)

根据信息进入后台























## 预览

### 例站

[https://share.lanol.cn](https://share.lanol.cn)

### 暗黑模式

<table style="width:100%">

<tr style="width: 100%">
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_10.png" alt="寄文件">

</td>
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_11.png" alt="寄文件">

</td>
</tr>
</table>

### 寄件

<table style="width: 100%">
<tr style="width: 100%">
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_1.png" alt="寄文件">
</td>
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_2.png" alt="寄文本">
</td>
</tr>
<tr style="width: 100%;">
<td colspan="2" style="width: 100%;">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_3.png" alt="寄文本">
</td>
</tr>
</table>

### 取件

<table style="width: 100%">
<tr style="width: 100%">
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_6.png" alt="取件">
</td>
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_5.png" alt="取件码错误">
</td>
</tr>
<tr style="width: 100%;">
<td colspan="2" style="width: 100%;">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_4.png" alt="取文件">
</td>
</tr>
</table>

### 管理

<table style="width: 100%">
<tr style="width: 100%">
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_7.png" alt="admin">
</td>
<td style="width: 50%">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_12.png" alt="admin">
</td>
</tr>
<tr style="width: 100%;">
<td colspan="2" style="width: 100%;">
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_13.png" alt="admin">
</td>
</tr>
</table>

## 配置文件

如果需要修改配置，在项目同目录下新建一个`data`文件夹，然后在创建`.env`文件，重启即可

```dotenv
# 端口
PORT=12345
# Sqlite数据库文件
DATABASE_URL=sqlite+aiosqlite:///database.db
# 静态文件夹
DATA_ROOT=./static
# 静态文件夹URL
STATIC_URL=/static
# 开启上传
ENABLE_UPLOAD=True
# 错误次数
ERROR_COUNT=5
# 错误限制分钟数
ERROR_MINUTE=10
# 上传次数
UPLOAD_COUNT=60
# 上传限制分钟数
UPLOAD_MINUTE=1
# 删除过期文件的间隔（分钟）
DELETE_EXPIRE_FILES_INTERVAL=10
# 管理地址
ADMIN_ADDRESS=admin
# 管理密码
ADMIN_PASSWORD=admin
# 文件大小限制，默认10MB
FILE_SIZE_LIMIT=10
# 网站标题
TITLE=文件快递柜
# 网站描述
DESCRIPTION=FileCodeBox，文件快递柜，口令传送箱，匿名口令分享文本，文件，图片，视频，音频，压缩包等文件
# 网站关键词
KEYWORDS=FileCodeBox，文件快递柜，口令传送箱，匿名口令分享文本，文件，图片，视频，音频，压缩包等文件
# 存储引擎
STORAGE_ENGINE=filesystem
# 如果使用阿里云OSS服务的话需要额外创建如下参数：
# 阿里云账号AccessKey
KeyId=阿里云账号AccessKey
# 阿里云账号AccessKeySecret
KeySecret=阿里云账号AccessKeySecret
# 阿里云OSS Bucket的地域节点
OSS_ENDPOINT=阿里云OSS Bucket的地域节点
# 阿里云OSS Bucket的BucketName
BUCKET_NAME=阿里云OSS Bucket的BucketName
```

## 接口文档

前端比较简陋，可以使用接口进行二次开发

### 取件

#### PATH

`/`

#### METHOD

`POST`

#### PARAMS

code: 取件码

#### Response

```json
{
  "detail": "msg",
  "data": {
    "type": "类型",
    "text": "文本",
    "name": "名称",
    "code": "取件码"
  }
}
```

### 寄件

#### PATH

`/share`

#### METHOD

`POST`

#### PARAMS

style: 1为次数，2为时间
value: 次数或时间
text: 取件码
file: 文件

#### Response

```json
{
  "detail": "msg",
  "data": {
    "code": "类型",
    "key": "唯一ID",
    "name": "名称"
  }
}
```

## 状态

![Alt](https://repobeats.axiom.co/api/embed/7a6c92f1d96ee57e6fb67f0df371528397b0c9ac.svg "Repobeats analytics image")

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=vastsa/FileCodeBox&type=Date)](https://star-history.com/#vastsa/FileCodeBox&Date)

## 赞赏

<table style="width: 100%">
<tr style="width: 100%">
<td style="width: 50%;text-align: center;">
支付宝
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_9.png" alt="支付宝">
</td>
<td style="width: 50%;text-align: center">
微信
<img src="https://fastly.jsdelivr.net/gh/vastsa/FileCodeBox@V1.6/images/img_8.png" alt="微信">
</td>
</tr>
</table>    

## 常见问题

1. 413 Request Entity Too Large
   Nginx限制：
   找到自己主机的nginx.conf配置文件，打开
   在http{}中加入 client_max_body_size 10m;
   然后重启nginx
2. 

## 免责声明

本项目开源仅供学习使用，不得用于任何违法用途，否则后果自负，与本人无关。使用请保留项目地址谢谢。
