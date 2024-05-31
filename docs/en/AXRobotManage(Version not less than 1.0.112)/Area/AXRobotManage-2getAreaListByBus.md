# getAreaListByBus

## Method

## `getAreaListByBus(businessId) -> {Promise.<any>}`

Obtain region list based on business ID

### Parameters

| Fields       | Type | Description     |
| ------------ | -------| -------- |
| `businessId` | string |  businessId |

### Return Value `Promise.<any>`

| Fields       | Type | Description     |
| ------------ | ------------- | --------------  |
| `buildingId` | String        | buildingId         |
| `businessId` | String        | businessId         |
| `floor`      | Integer       | floor             |
| `floorName`  | String        | floorName           |
| `id`         | String        | id             |
| `name`       | String        | name             |
| `createTime` | Integer       | createTime          |


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


