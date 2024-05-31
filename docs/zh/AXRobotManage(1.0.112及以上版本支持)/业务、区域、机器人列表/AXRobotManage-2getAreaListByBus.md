# 根据业务id获取区域列表

## 方法

## `getAreaListByBus(businessId) -> {Promise.<any>}`

根据业务id获取区域列表

### 参数

| 名称         | 类型    | 说明     |
| ------------ | -------| -------- |
| `businessId` | string |  业务标识 |

### 返回值 `Promise.<any>`

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `buildingId` | String        | 建筑标识         |
| `businessId` | String        | 业务名称         |
| `floor`      | Integer       | 楼层             |
| `floorName`  | String        | 楼层名           |
| `id`         | String        | 标识             |
| `name`       | String        | 名称             |
| `createTime` | Integer       | 创建时间          |


### 请求示例

```javascript
...
let result = await axRobot.getAreaListByBus(businessId)
if (result && result.data) {
	let areaList =  result.data.list
	...
}
...
```

### 响应数据示例

```JSON
...
	"data": {
        "count": 1,
        "list": [
            {
                "buildingId": "<buildingId>",
                "businessId": "<businessId>",
                "createTime": 1700440085026,
                "floor": 16,
                "floorName": "<floorName>",
                "id": "<id>",
                "name": "<name>",
                "version": "<version>"
            },
			...
        ]
    }
...
```


