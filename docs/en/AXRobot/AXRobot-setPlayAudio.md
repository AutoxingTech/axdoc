# Set Play Audio

## `setPlayAudio(playAudio) -> {Promise.<boolean>}`

Set Play Audio

### Parameters

| Name  | Data Type | Description |
| ------ | ------ | ------------------------ |
| `playAudio` | [PlayAudio](../../Define/Define-PlayAudio) | Play Audio |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript 
...
let playAudio = {
    mode: 1,
    url: "",
    audioId: "38001",
    volume: 10,
    interval: -1,
    num: 1,
    duration: 5
}
const success = await axRobot.setPlayAudio(playAudio);
...
```

