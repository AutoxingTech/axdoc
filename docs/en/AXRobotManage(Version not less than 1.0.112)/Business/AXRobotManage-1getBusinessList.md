# Get Business List

## Method

## `getBusinessList() -> {Promise.<any>}`

Get business list (without pagination, query all business lists)

### Parameters

None

### Return Value `Promise.<any>`

res.data：

| Fields         | Type             | Description                         |
| ------------ | --------------- | ---------------------------  |
| `groups`     | Array          | Data Business Group List                   |
| `lists`      | Array          | Business List (businessInfo objects are as follows)|

businessInfo：

| Fields         | Type           | Description            |
| ------------ | ------------- | --------------  |
| `id`         | String        | Business id         |
| `name`       | String        | Business name         |
| `type`       | Integer       | BusinessType 1- restaurant 2- hotel 3- disinfection and sterilization 4- office building 5- factory  |
| `address`    | String        | Business address     |
| `customerId` | String        | Business customerId  |
| `buildingId` | String        | buildingId  |
| `createTime` | Integer       | createTime          |


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


