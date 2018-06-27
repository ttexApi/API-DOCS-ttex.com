## API参考
### 交易API
1. Get/currency/trade/cancel删除订单

URL ```https://api.ttex.com/currency/trade/cancel```
示例
```
# Request
GET https://api.ttex.com/currency/trade/cancel
# Response
{
	"data":"委托撤单成功",
	"result":success
}
```
返回值说明
```
data:委托撤单成功
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| txNo|  String |  是  | 当前选择撤销订单号|
2. Get/currency/trade/findHistoryEntrust获取个人历史委托

URL ```  https://api.ttex.com/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findHistoryEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/currency/trade/findEntrust获取个人当前委托

URL ```https://api.ttex.com/currency/trade/findEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
4. Get/public/stock/get获取交易盘口

URL ```https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{
	"data:{
	"price":0.00252621
	"priceFluctuation":4.52
	},
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的对象
price:价格
priceFluctuation:占比
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/marketDepth获取交易盘口数据

URL ``` https://api.ttex.com/public/stock/marketDepth```
示例
```
# Request
GET https://api.ttex.com/public/stock/marketDepth
# Response
{
  "buyers":[{
  "amountStr":59.2182
  "priceStr":0.0025201500
  }],
  "sellers":[{
  "amountStr":13.2563
  "priceStr":0.0025275500
  }],
}
```
返回值说明
```
buyers:请求返回成功取到的数组对象
sellers:请求返回成功取到的数组对象
amountStr:数量
priceStr:价格
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| num|  number|  是  |盘口显示数据量|
6. Get/public/stock/currency/trade/latest交易记录

URL ```https://api.ttex.com/public/stock/currency/trade/latest```
示例
```
# Request
GET   https://api.ttex.com/public/stock/currency/trade/latest
# Response
[{
    "num":303.6577
    "tradePrice":0.00000739
    "tradeTime":1529568810638
}]
```
返回值说明
```
num:成交数量
tradePrice:成交价格
tradeTime:成交时间
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
7. Get/member/position/getWithCurrency获取当前交易对余额

URL ```https://api.ttex.com/member/position/getWithCurrency```
示例
```
# Request
GET https://api.ttex.com/member/position/getWithCurrency
# Response
{
        "buyBalance":99999998.3391
        "sellBalance":0.000000
}
```
返回值说明
```
buyBalance:买入时余额
sellBalance:买入时余额
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/public/stock/findBySector获取首页列表

URL ``` https://api.ttex.com/public/stock/findBySector```
示例
```
# Request
GET  https://api.ttex.com/public/stock/findBySector
# Response
[{
        "price":0.000019
        "priceFluctuation":0
        "tokenIdentification":TTF
}]
```
返回值说明
```
price:价格
priceFluctuation:涨跌幅	
tokenIdentification:币种
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|sectorId |  number   |   是     |   sectorId=2时根据BTC  |
|v         |       number  |  是       |  v=0.5570646255753278|
9. Get/mobile/currency/trade/market/buy市价交易买入

URL ```  https://api.ttex.com/currency/trade/market/buy```
示例
```
# Request
GET   https://api.ttex.com/currency/trade/market/buy
# Response
[{
        "txNo":15300629835086
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|amount|  number   |   是     |	买入量	  |
|code |  number  |  是       |  币种名称	|
10. Get/mobile/currency/trade/market/sell市价交易卖出

URL ```   https://api.ttex.com/currency/trade/market/sell```
示例
```
# Request
GET    https:api.ttex.com/currency/trade/market/sell
# Response
[{
        "txNo":153006298350861212
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	卖出量	  |
|code |  number  |  是       |  币种名称	|
11. Get/mobile/currency/trade/buy限价交易买入

URL ```https://api.ttex.com/currency/trade/buy```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/buy
# Response
[{
        "txNo":1530063601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price | number|是|限价买入价格
12. Get/mobile/currency/trade/sell限价交易卖出

URL ```    https://api.ttex.com/currency/trade/sell```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/sell
# Response
[{
        "txNo":1512263601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price| number|是|价格
###资产API
1. Get/currency/deposits/find充值记录

URL ```  https://api.ttex.com/currency/deposits/find```
示例
```
# Request
GET https://api.ttex.com/currency/deposits/find
# Response
{
     "data":[{
     "amount":10000
     "confirmTimeThreshold":1
     "confirmTimes":1
     "createTimeString":2018-06-02 17:35:45
     "flow":1
     "txNo":20180602583955
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
amount:数量
createTimeString:充币时间
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type  |           |   是        |  type=0       |
2. Get/ewallet/ewalletAddress/findCurrencyDepositAddress充币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress
# Response
{
     "data":[{
     "address":0xc298fe018e00db3670fdf3ed4b5ff7f1f06397cd
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
address:地址
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/ewallet/ewalletAddress/delete删除提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/delete```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/delete
# Response
{
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| ids|  number|  是  | 提币地址|
4. Get/currency/withdraws/save提币

URL ```   https://www.api.com/currency/withdraws/save```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/save
# Response
{    
     "data":提交成功
     "result":success
}
```
返回值说明
```
data:提交成功
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| amount|  number|  是  | 提币数量	|
| 	captcha|  number|  是  | 	验证码|
| pwd|  string|  是  |	资金密码	|
|toEwalletAddress|  string|  是  | 提币地址	|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/get提币手续费

URL ```   https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{  
     "data":{
     "currencyPoundage":0.01
     }
     "result":success
}
```
返回值说明
```
data:请求成功返回的对象
currencyPoundage:提币手续费
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
6. Get/currency/withdraws/find提币记录

URL ``` https://api.ttex.com/currency/withdraws/find```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/find
# Response
{  
     "data":[{
     "amount":5
     "createTimeString":2018-06-11 15:11:40
     "flow":1
     "toEwalletAddress":212
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
amount:数量
createTimeString:时间
flow:状态
toEwalletAddress:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type    |  number    | 是     | type=0      |
7. Get/ewallet/ewalletAddress/find显示提币地址

URL ``` https://api.ttex.com/ewallet/ewalletAddress/find```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/find
# Response
{  
     "data":[{
     "address":111
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
address:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/ewallet/ewalletAddress/save添加提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/save```
示例
```
# Request
GET   https://api.ttex.com/ewallet/ewalletAddress/save
# Response
{  
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| address|  String |  是  | 提币地址 |
9. Get/member/getAccount资产中心

URL ```https://api.ttex.com/member/getAccount```
示例
```
# Request
GET https://api.ttex.com/member/getAccount
# Response
[{  
     "blockedNum":0
     "holdingAmount":100000000.00000000000000
     "marketValue":85774.00000000
     "name":HSR
     "totalNum":100000000
}]
```
返回值说明
```
blockedNum:冻结资产
holdingAmount:总计
marketValue:估值
name:币种
totalNum:可用余额
```












## API参考
### 交易API
1. Get/currency/trade/cancel删除订单

URL ```https://api.ttex.com/currency/trade/cancel```
示例
```
# Request
GET https://api.ttex.com/currency/trade/cancel
# Response
{
	"data":"委托撤单成功",
	"result":success
}
```
返回值说明
```
data:委托撤单成功
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| txNo|  String |  是  | 当前选择撤销订单号|
2. Get/currency/trade/findHistoryEntrust获取个人历史委托

URL ```  https://api.ttex.com/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findHistoryEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/currency/trade/findEntrust获取个人当前委托

URL ```https://api.ttex.com/currency/trade/findEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
4. Get/public/stock/get获取交易盘口

URL ```https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{
	"data:{
	"price":0.00252621
	"priceFluctuation":4.52
	},
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的对象
price:价格
priceFluctuation:占比
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/marketDepth获取交易盘口数据

URL ``` https://api.ttex.com/public/stock/marketDepth```
示例
```
# Request
GET https://api.ttex.com/public/stock/marketDepth
# Response
{
  "buyers":[{
  "amountStr":59.2182
  "priceStr":0.0025201500
  }],
  "sellers":[{
  "amountStr":13.2563
  "priceStr":0.0025275500
  }],
}
```
返回值说明
```
buyers:请求返回成功取到的数组对象
sellers:请求返回成功取到的数组对象
amountStr:数量
priceStr:价格
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| num|  number|  是  |盘口显示数据量|
6. Get/public/stock/currency/trade/latest交易记录

URL ```https://api.ttex.com/public/stock/currency/trade/latest```
示例
```
# Request
GET   https://api.ttex.com/public/stock/currency/trade/latest
# Response
[{
    "num":303.6577
    "tradePrice":0.00000739
    "tradeTime":1529568810638
}]
```
返回值说明
```
num:成交数量
tradePrice:成交价格
tradeTime:成交时间
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
7. Get/member/position/getWithCurrency获取当前交易对余额

URL ```https://api.ttex.com/member/position/getWithCurrency```
示例
```
# Request
GET https://api.ttex.com/member/position/getWithCurrency
# Response
{
        "buyBalance":99999998.3391
        "sellBalance":0.000000
}
```
返回值说明
```
buyBalance:买入时余额
sellBalance:买入时余额
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/public/stock/findBySector获取首页列表

URL ``` https://api.ttex.com/public/stock/findBySector```
示例
```
# Request
GET  https://api.ttex.com/public/stock/findBySector
# Response
[{
        "price":0.000019
        "priceFluctuation":0
        "tokenIdentification":TTF
}]
```
返回值说明
```
price:价格
priceFluctuation:涨跌幅	
tokenIdentification:币种
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|sectorId |  number   |   是     |   sectorId=2时根据BTC  |
|v         |       number  |  是       |  v=0.5570646255753278|
9. Get/mobile/currency/trade/market/buy市价交易买入

URL ```  https://api.ttex.com/currency/trade/market/buy```
示例
```
# Request
GET   https://api.ttex.com/currency/trade/market/buy
# Response
[{
        "txNo":15300629835086
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|amount|  number   |   是     |	买入量	  |
|code |  number  |  是       |  币种名称	|
10. Get/mobile/currency/trade/market/sell市价交易卖出

URL ```   https://api.ttex.com/currency/trade/market/sell```
示例
```
# Request
GET    https:api.ttex.com/currency/trade/market/sell
# Response
[{
        "txNo":153006298350861212
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	卖出量	  |
|code |  number  |  是       |  币种名称	|
11. Get/mobile/currency/trade/buy限价交易买入

URL ```https://api.ttex.com/currency/trade/buy```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/buy
# Response
[{
        "txNo":1530063601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price | number|是|限价买入价格
12. Get/mobile/currency/trade/sell限价交易卖出

URL ```    https://api.ttex.com/currency/trade/sell```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/sell
# Response
[{
        "txNo":1512263601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price| number|是|价格
###资产API
1. Get/currency/deposits/find充值记录

URL ```  https://api.ttex.com/currency/deposits/find```
示例
```
# Request
GET https://api.ttex.com/currency/deposits/find
# Response
{
     "data":[{
     "amount":10000
     "confirmTimeThreshold":1
     "confirmTimes":1
     "createTimeString":2018-06-02 17:35:45
     "flow":1
     "txNo":20180602583955
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
amount:数量
createTimeString:充币时间
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type  |           |   是        |  type=0       |
2. Get/ewallet/ewalletAddress/findCurrencyDepositAddress充币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress
# Response
{
     "data":[{
     "address":0xc298fe018e00db3670fdf3ed4b5ff7f1f06397cd
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
address:地址
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/ewallet/ewalletAddress/delete删除提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/delete```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/delete
# Response
{
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| ids|  number|  是  | 提币地址|
4. Get/currency/withdraws/save提币

URL ```   https://www.api.com/currency/withdraws/save```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/save
# Response
{    
     "data":提交成功
     "result":success
}
```
返回值说明
```
data:提交成功
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| amount|  number|  是  | 提币数量	|
| 	captcha|  number|  是  | 	验证码|
| pwd|  string|  是  |	资金密码	|
|toEwalletAddress|  string|  是  | 提币地址	|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/get提币手续费

URL ```   https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{  
     "data":{
     "currencyPoundage":0.01
     }
     "result":success
}
```
返回值说明
```
data:请求成功返回的对象
currencyPoundage:提币手续费
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
6. Get/currency/withdraws/find提币记录

URL ``` https://api.ttex.com/currency/withdraws/find```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/find
# Response
{  
     "data":[{
     "amount":5
     "createTimeString":2018-06-11 15:11:40
     "flow":1
     "toEwalletAddress":212
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
amount:数量
createTimeString:时间
flow:状态
toEwalletAddress:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type    |  number    | 是     | type=0      |
7. Get/ewallet/ewalletAddress/find显示提币地址

URL ``` https://api.ttex.com/ewallet/ewalletAddress/find```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/find
# Response
{  
     "data":[{
     "address":111
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
address:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/ewallet/ewalletAddress/save添加提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/save```
示例
```
# Request
GET   https://api.ttex.com/ewallet/ewalletAddress/save
# Response
{  
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| address|  String |  是  | 提币地址 |
9. Get/member/getAccount资产中心

URL ```https://api.ttex.com/member/getAccount```
示例
```
# Request
GET https://api.ttex.com/member/getAccount
# Response
[{  
     "blockedNum":0
     "holdingAmount":100000000.00000000000000
     "marketValue":85774.00000000
     "name":HSR
     "totalNum":100000000
}]
```
返回值说明
```
blockedNum:冻结资产
holdingAmount:总计
marketValue:估值
name:币种
totalNum:可用余额
```












## API参考
### 交易API
1. Get/currency/trade/cancel删除订单

URL ```https://api.ttex.com/currency/trade/cancel```
示例
```
# Request
GET https://api.ttex.com/currency/trade/cancel
# Response
{
	"data":"委托撤单成功",
	"result":success
}
```
返回值说明
```
data:委托撤单成功
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| txNo|  String |  是  | 当前选择撤销订单号|
2. Get/currency/trade/findHistoryEntrust获取个人历史委托

URL ```  https://api.ttex.com/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findHistoryEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/currency/trade/findEntrust获取个人当前委托

URL ```https://api.ttex.com/currency/trade/findEntrust ```
示例
```
# Request
GET https://api.ttex.com/currency/trade/findEntrust
# Response
{
	"data:[{
	"createTimeString":2018-06-21 15:23:44
	"entrustNumber":12407980.8629
	"entrustPrice":0.08059329
	"tradeMark":0
	"tradeStatus":5
	}],
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的数组对象
createTimeString:时间
entrustNumber:数量
entrustPrice:价格
tradeMark:类型
tradeStatus:状态
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
4. Get/public/stock/get获取交易盘口

URL ```https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{
	"data:{
	"price":0.00252621
	"priceFluctuation":4.52
	},
	"result":success
}
```
返回值说明
```
data:请求返回成功取到的对象
price:价格
priceFluctuation:占比
result:成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/marketDepth获取交易盘口数据

URL ``` https://api.ttex.com/public/stock/marketDepth```
示例
```
# Request
GET https://api.ttex.com/public/stock/marketDepth
# Response
{
  "buyers":[{
  "amountStr":59.2182
  "priceStr":0.0025201500
  }],
  "sellers":[{
  "amountStr":13.2563
  "priceStr":0.0025275500
  }],
}
```
返回值说明
```
buyers:请求返回成功取到的数组对象
sellers:请求返回成功取到的数组对象
amountStr:数量
priceStr:价格
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| num|  number|  是  |盘口显示数据量|
6. Get/public/stock/currency/trade/latest交易记录

URL ```https://api.ttex.com/public/stock/currency/trade/latest```
示例
```
# Request
GET   https://api.ttex.com/public/stock/currency/trade/latest
# Response
[{
    "num":303.6577
    "tradePrice":0.00000739
    "tradeTime":1529568810638
}]
```
返回值说明
```
num:成交数量
tradePrice:成交价格
tradeTime:成交时间
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
7. Get/member/position/getWithCurrency获取当前交易对余额

URL ```https://api.ttex.com/member/position/getWithCurrency```
示例
```
# Request
GET https://api.ttex.com/member/position/getWithCurrency
# Response
{
        "buyBalance":99999998.3391
        "sellBalance":0.000000
}
```
返回值说明
```
buyBalance:买入时余额
sellBalance:买入时余额
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/public/stock/findBySector获取首页列表

URL ``` https://api.ttex.com/public/stock/findBySector```
示例
```
# Request
GET  https://api.ttex.com/public/stock/findBySector
# Response
[{
        "price":0.000019
        "priceFluctuation":0
        "tokenIdentification":TTF
}]
```
返回值说明
```
price:价格
priceFluctuation:涨跌幅	
tokenIdentification:币种
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|sectorId |  number   |   是     |   sectorId=2时根据BTC  |
|v         |       number  |  是       |  v=0.5570646255753278|
9. Get/mobile/currency/trade/market/buy市价交易买入

URL ```  https://api.ttex.com/currency/trade/market/buy```
示例
```
# Request
GET   https://api.ttex.com/currency/trade/market/buy
# Response
[{
        "txNo":15300629835086
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|amount|  number   |   是     |	买入量	  |
|code |  number  |  是       |  币种名称	|
10. Get/mobile/currency/trade/market/sell市价交易卖出

URL ```   https://api.ttex.com/currency/trade/market/sell```
示例
```
# Request
GET    https:api.ttex.com/currency/trade/market/sell
# Response
[{
        "txNo":153006298350861212
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	卖出量	  |
|code |  number  |  是       |  币种名称	|
11. Get/mobile/currency/trade/buy限价交易买入

URL ```https://api.ttex.com/currency/trade/buy```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/buy
# Response
[{
        "txNo":1530063601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price | number|是|限价买入价格
12. Get/mobile/currency/trade/sell限价交易卖出

URL ```    https://api.ttex.com/currency/trade/sell```
示例
```
# Request
GET     https://api.ttex.com/currency/trade/sell
# Response
[{
        "txNo":1512263601833776402
        "result":3000
}]
```
返回值说明
```
result:是否成功
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
|num|  number   |   是     |	限价买入量	  |
|code |  number  |  是       |  币种名称	|
|price| number|是|价格
###资产API
1. Get/currency/deposits/find充值记录

URL ```  https://api.ttex.com/currency/deposits/find```
示例
```
# Request
GET https://api.ttex.com/currency/deposits/find
# Response
{
     "data":[{
     "amount":10000
     "confirmTimeThreshold":1
     "confirmTimes":1
     "createTimeString":2018-06-02 17:35:45
     "flow":1
     "txNo":20180602583955
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
amount:数量
createTimeString:充币时间
txNo:订单号
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type  |           |   是        |  type=0       |
2. Get/ewallet/ewalletAddress/findCurrencyDepositAddress充币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/findCurrencyDepositAddress
# Response
{
     "data":[{
     "address":0xc298fe018e00db3670fdf3ed4b5ff7f1f06397cd
     }],
     "result":success
}
```
返回值说明
```
data:返回成功时的数组对象
address:地址
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
3. Get/ewallet/ewalletAddress/delete删除提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/delete```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/delete
# Response
{
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| ids|  number|  是  | 提币地址|
4. Get/currency/withdraws/save提币

URL ```   https://www.api.com/currency/withdraws/save```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/save
# Response
{    
     "data":提交成功
     "result":success
}
```
返回值说明
```
data:提交成功
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| amount|  number|  是  | 提币数量	|
| 	captcha|  number|  是  | 	验证码|
| pwd|  string|  是  |	资金密码	|
|toEwalletAddress|  string|  是  | 提币地址	|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
5. Get/public/stock/get提币手续费

URL ```   https://api.ttex.com/public/stock/get```
示例
```
# Request
GET https://api.ttex.com/public/stock/get
# Response
{  
     "data":{
     "currencyPoundage":0.01
     }
     "result":success
}
```
返回值说明
```
data:请求成功返回的对象
currencyPoundage:提币手续费
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
6. Get/currency/withdraws/find提币记录

URL ``` https://api.ttex.com/currency/withdraws/find```
示例
```
# Request
GET  https://api.ttex.com/currency/withdraws/find
# Response
{  
     "data":[{
     "amount":5
     "createTimeString":2018-06-11 15:11:40
     "flow":1
     "toEwalletAddress":212
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
amount:数量
createTimeString:时间
flow:状态
toEwalletAddress:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
| type    |  number    | 是     | type=0      |
7. Get/ewallet/ewalletAddress/find显示提币地址

URL ``` https://api.ttex.com/ewallet/ewalletAddress/find```
示例
```
# Request
GET  https://api.ttex.com/ewallet/ewalletAddress/find
# Response
{  
     "data":[{
     "address":111
     }]
     "result":success
}
```
返回值说明
```
data:请求成功返回的数组对象
address:地址
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
8. Get/ewallet/ewalletAddress/save添加提币地址

URL ```  https://api.ttex.com/ewallet/ewalletAddress/save```
示例
```
# Request
GET   https://api.ttex.com/ewallet/ewalletAddress/save
# Response
{  
     "result":success
}
```
返回值说明
```
result:返回是否成功
```
请求参数

|参数名    |     参数类型 |   必填  |  描述 |
| :-------- | --------:| :------: |:------:|
| address|  String |  是  | 提币地址 |
9. Get/member/getAccount资产中心

URL ```https://api.ttex.com/member/getAccount```
示例
```
# Request
GET https://api.ttex.com/member/getAccount
# Response
[{  
     "blockedNum":0
     "holdingAmount":100000000.00000000000000
     "marketValue":85774.00000000
     "name":HSR
     "totalNum":100000000
}]
```
返回值说明
```
blockedNum:冻结资产
holdingAmount:总计
marketValue:估值
name:币种
totalNum:可用余额
```












