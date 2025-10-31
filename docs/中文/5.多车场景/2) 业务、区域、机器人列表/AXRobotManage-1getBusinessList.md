# 获取业务列表

## 方法

## `getBusinessList() -> {Promise.<any>}`

获取业务列表(没有分页，查询全部业务列表)

### 参数

无

### 返回值 `Promise.<any>`

res.data：

| 名称         | 类型             | 说明                         |
| ------------ | --------------- | ---------------------------  |
| `groups`     | Array          | 数业务组列表                   |
| `lists`      | Array          | 业务列表（businessInfo对象如下）|

businessInfo：

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `id`         | String        | 业务标识         |
| `name`       | String        | 业务名称         |
| `type`       | Integer       | 业务类型 1 - 餐厅 2 - 酒店 3 - 消杀 4 - 写字楼 5 - 工厂  |
| `address`    | String        | 业务所在地址     |
| `customerId` | String        | 业务所有者标识    |
| `buildingId` | String        | 业务所在楼宇标识  |
| `createTime` | Integer       | 创建时间          |


### 请求示例

```javascript
...
let result = await axRobot.getBusinessList()
if (result && result.data) {
	let businessList =  result.data.lists
	...
}
...
```

### 响应数据示例

```JSON
...
	"data": {
	"lists": [
		{
			"id": "62f320052a97efd436662a4a",
			"name": "string",
			"type": 0,
			"address": "string",
			"customerId": "oHrGS5YitT4Uq3mvBnrkIE1nhnjg",
			"buildingId": "60a4c374059acc6c8bdff074",
			"createTime": 1660100613000
		},
		...
	],
	"groups": [{
		"id": "01/1c2fe984-fc34-4d62-8b06-896d029ef240",
		"name": "string",
		"ownerCode": "string",
		"createTime": 0,
		"updateTime": 0,
		"busList": [{
			"busId": "string",
			"busName": "string"
		}]
	}]
}
...
```


