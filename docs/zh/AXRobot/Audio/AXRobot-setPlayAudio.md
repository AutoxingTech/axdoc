# 设置音频播报

## `setPlayAudio(playAudio) -> {Promise.<boolean>}`

设置音频播报

### 参数

| 名称   | 类型   | 说明                     |
| ------ | ------ | ------------------------ |
| `playAudio` | [PlayAudio](../../../Define/Define-PlayAudio) | 播报音频 |

### 返回值 `Promise.<boolean>`

是否成功

* true - 成功
* false - 失败

### 示例

```typescript
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

