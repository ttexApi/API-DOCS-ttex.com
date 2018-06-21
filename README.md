## API参考
### 交易API
1. Get/mobile/currency/trade/cancel删除订单

URL ```https://www.ttex.com/mobile/currency/trade/cancel```
示例
```
# Request
GET https://ttex.com/mobile/currency/trade/cancel
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
2. Get/mobile/currency/trade/findHistoryEntrust获取个人历史委托

URL ```  https://www.ttex.com/mobile/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://ttex.com/mobile/currency/trade/findHistoryEntrust
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
3. Get/mobile/currency/trade/findEntrust获取个人当前委托

URL ```https://www.ttex.com/mobile/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://ttex.com/mobile/currency/trade/findHistoryEntrust
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

URL ```https://www.ttex.com/public/stock/get```
示例
```
# Request
GET https://www.ttex.com/public/stock/get
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

URL ``` https://www.ttex.com/public/stock/marketDepth```
示例
```
# Request
GET  https://www.ttex.com/public/stock/marketDepth
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

URL ```https://www.ttex.com/public/stock/currency/trade/latest```
示例
```
# Request
GET   https://www.ttex.com/public/stock/currency/trade/latest
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
7. Get/mobile/member/position/getWithCurrency获取当前交易对余额

URL ```https://www.ttex.com/mobile/member/position/getWithCurrency```
示例
```
# Request
GET   https://www.ttex.com/mobile/member/position/getWithCurrency
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

URL ``` https://www.ttex.com/public/stock/findBySector```
示例
```
# Request
GET    https://www.ttex.com/public/stock/findBySector
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
| symbol|  String |  是  | btc_usd ltc_usd eth_usd etc_usd bch_usd|
|sectorId       |  number   |   是     |   sectorId=2时根据BTC  |
|v         |       number  |  是       |  v=0.5570646255753278





