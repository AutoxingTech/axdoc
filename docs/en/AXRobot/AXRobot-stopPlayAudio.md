# Stop Play Audio

## `stopPlayAudio(mode) -> {Promise.<boolean>}`

Stop play audio

### Parameters

| Name   | Type   | Description                        |
| ------ | ------ | ---------------------------------- |
| `mode` | number | 1 - Upper Mochine<br />2 - Chassis |

### Return Value `Promise.<boolean>`

Whether the executiion is successful

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.stopPlayAudio(1);
...
```

