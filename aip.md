# 接口文档

## 线路模糊搜索

> url: http://www.zhbuswx.com/Handlers/BusQuery.ashx?handlerName=GetLineListByLineName&key=1&_=1536678579892

### 方法 get

| 参数        | 值                          |
| :---------- | :-------------------------- |
| handlerName | 这个应该是获取列表的        |
| key         | 当前输入值                  |
| _          | 时间戳 |

```
{
	"flag": 1002,
	"data": [{
		"Id": "6b3b3940-7c0f-414d-a5c9-90bb05408b21",
		"Name": "5路",
		"LineNumber": "5路",
		"Direction": 0,
		"FromStation": "海虹总站",
		"ToStation": "湾仔",
		"BeginTime": "06:20",
		"EndTime": "23:10",
		"Price": "2",
		"Interval": "8.1",
		"Description": "",
		"StationCount": 34
	}, {
		"Id": "958cf200-9865-4772-8fb4-e015ebb23f67",
		"Name": "5路",
		"LineNumber": "5路",
		"Direction": 1,
		"FromStation": "湾仔",
		"ToStation": "海虹总站",
		"BeginTime": "06:15",
		"EndTime": "22:45",
		"Price": "2",
		"Interval": "8.1",
		"Description": "",
		"StationCount": 33
	}]
}
```
### json 解释

|名字|值|
|:---|:-|
|Id|未知|
|Name|线路名称|
|Direction|可能是排序,可能是方向 (0,1)|
|FromStation|起点|
|ToStation|终点|
|BeginTime|开始运营的时间|
|EndTime|结束运营时间|
|Price|价钱(单位:元)|
|Description|描述|
|StationCount|总站数|

## 线路详情信息

> url:http://www.zhbuswx.com/Handlers/BusQuery.ashx?handlerName=GetBusListOnRoad&lineName=26%E8%B7%AF&fromStation=%E6%99%AE%E9%99%80%E5%AF%BA

### GET

|名字|值|
|:-|:-|
|handlerName|请求模式(GetBusListOnRoad)|
|lineName|线路名称(url转码)|
|fromStation|线路起始点(url转码)|