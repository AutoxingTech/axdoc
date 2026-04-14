````markdown
# Get Business List

## Method

## `getBusinessList() -> {Promise.<any>}`

Get business list (no pagination, returns all business lists)

### Parameters

None

### Return Value `Promise.<any>`

res.data:

| Name         | Type             | Description                         |
| ------------ | --------------- | ---------------------------  |
| `groups`     | Array          | Business group list                   |
| `lists`      | Array          | Business list (businessInfo object as below)|

businessInfo:

| Name         | Type           | Description            |
| ------------ | ------------- | --------------  |
| `id`         | String        | Business identifier         |
| `name`       | String        | Business name         |
| `type`       | Integer       | Business type 1 - Restaurant 2 - Hotel 3 - Disinfection 4 - Office Building 5 - Factory  |
| `address`    | String        | Business address     |
| `customerId` | String        | Business owner identifier    |
| `buildingId` | String        | Building identifier  |
| `createTime` | Integer       | Creation time          |


### Request Example

```javascript
...
let result = await axRobot.getBusinessList()
if (result && result.data) {
	let businessList =  result.data.lists
	...
}
...
```

### Response Data Example

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



````
