# setQueueOrder

## Method

## `setQueueOrder(key, newOrder) -> {Promise.<boolean>}`

Set the sorting of the entire task queue.

### Parameters

| Fields         | Type           | Description            |
| --------- | ---------------------- | ------------------      |
| `key`     | string                 |key |
| `newOrder`| Array<string>          | newOrder      |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.setQueueOrder(key, ["string", "string"]);
...
```



