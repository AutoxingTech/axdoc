# continueQueue

## Method

## `continueQueue(key) -> {Promise.<boolean>}`

Continue task list to assign tasks.

### Parameters

| Fields         | Type           | Description            |
| ------ | ----------------------------- | -------- |
| `key` | string | key |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.continueQueue(key);
...
```



