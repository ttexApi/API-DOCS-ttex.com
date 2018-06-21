## API参考
### 交易API
1. Get/mobile/currency/trade/cancel删除订单

URL ```https://www.ttex.com/mobile/currency/trade/cancel```
示例
```
# Request
GET https://ttex.com/mobile/currency/trade/cancel?txNo=?
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
GET https://ttex.com/mobile/currency/trade/findHistoryEntrust?code=300020&page=0&limit=100
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
| symbol|  String |  是  | 币种编号|
3. Get/mobile/currency/trade/findEntrust获取个人当前委托

URL ```https://www.ttex.com/mobile/currency/trade/findHistoryEntrust ```
示例
```
# Request
GET https://ttex.com/mobile/currency/trade/findHistoryEntrust?code=300020&page=0&limit=100
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
| symbol|  String |  是  | 币种编号|
