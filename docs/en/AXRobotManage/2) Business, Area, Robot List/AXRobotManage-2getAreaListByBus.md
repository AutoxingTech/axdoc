````markdown
# Get Area List by Business ID

## Method

## `getAreaListByBus(businessId) -> {Promise.<any>}`

Get area list by business ID

### Parameters

| Name         | Type    | Description     |
| ------------ | -------| -------- |
| `businessId` | string |  Business identifier |

### Return Value `Promise.<any>`

| Name         | Type           | Description            |
| ------------ | ------------- | --------------  |
| `buildingId` | String        | Building identifier         |
| `businessId` | String        | Business name         |
| `floor`      | Integer       | Floor             |
| `floorName`  | String        | Floor name           |
| `id`         | String        | Identifier             |
| `name`       | String        | Name             |
| `createTime` | Integer       | Creation time          |


### Request Example

```javascript
...
let result = await axRobot.getAreaListByBus(businessId)
if (result && result.data) {
	let areaList =  result.data.list
	...
}
...
```

### Response Data Example

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



````
