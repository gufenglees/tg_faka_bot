## 介绍
这是一个Telegram 发卡机器人，此机器人基于Python开发，在Python 3.7运行环境测试通过。
Telegram 交流反馈群组：@tgfaka  [点击加入](https://t.me/tgfaka)

## 使用方法
### 第一次安装
#### 安装依赖
`pip3 install -r requirements.txt` 
#### 修改文件前缀
修改以`example.xxx.xxx`开头的文件，重命名为`xxx.xxx`。
例如`example.config.py`，重命名为`config.py`

需要重命名的文件为：`example.config.py`、`example.faka.sqlite3`、支付网关目录下的接口文件都需要重命名
#### 启动方法
`python3 main.py`
### 升级版本
[查看说明](https://github.com/lulafun/tg_faka_bot/wiki/%E7%89%88%E6%9C%AC%E5%8D%87%E7%BA%A7%E6%96%B9%E6%B3%95)

## 功能介绍
### 管理员界面
![](https://s3.jpg.cm/2020/08/01/bXuoT.png)
![](https://s3.jpg.cm/2020/06/29/cw0LC.jpg)
![](https://s3.jpg.cm/2020/06/29/cw2bt.jpg)
![](https://s3.jpg.cm/2020/06/29/cwg25.jpg)
![](https://s3.jpg.cm/2020/06/29/cwfNr.jpg)
![](https://s3.jpg.cm/2020/08/01/bXJVQ.png)
![](https://s3.jpg.cm/2020/08/01/bXtFh.png)
### 用户界面
![](https://s3.jpg.cm/2020/08/01/bX1DE.png)
![](https://s3.jpg.cm/2020/08/01/bXNyS.png)
### 数据库
使用sqlite3作为数据库，轻量、便于备份。

### 支付接口

#### 现有的支付接口

- 易支付
- 支付宝当面付
- mugglepay

由于市面上有许多的易支付版本，虽然接口传参一样，但是有些网站的返回值还是有所不同，目前该程序对我所使用过的易支付站点做了适配，如有不适配的情况，可以积极反馈

#### 配置自己的支付接口

编辑`config.py`文件
现在存在的支付接口：
```
PAYMENT_METHOD = {
    'epay': '支付宝/微信/QQ',
    'alifacepay': '支付宝当面付'
}
```

如果这时候有一个新的文件名为`mugglepay.py`的支付接口，那么可以这么配置：
```
PAYMENT_METHOD = {
    'epay': '支付宝/微信/QQ',
    'alifacepay': '支付宝当面付',
    'mugglepay': '加密货币'
}
```

`mugglepay.py`的相对路径为`getways/mugglepay/mugglepay.py`，请确保你安装了此插件需要的额外依赖

各个支付接口的配置已经整合到支付接口文件中，不再在`config.py`里面配置


#### 编写自己的支付接口
[查看教程](https://github.com/lulafun/tg_faka_bot/wiki/%E7%BC%96%E5%86%99%E8%87%AA%E5%B7%B1%E7%9A%84%E6%94%AF%E4%BB%98%E6%8E%A5%E5%8F%A3%E6%96%870707195%E4%BB%B6)