# 关闭背景音乐

## `stopPlayAudio(mode) -> {Promise.<boolean>}`

关闭背景音乐

### 参数

| 名称   | 类型   | 说明                     |
| ------ | ------ | ------------------------ |
| `mode` | number | 1 - 上位机<br />2 - 底盘 |

### 返回值 `Promise.<boolean>`

是否成功

* true - 成功
* false - 失败

### 示例

```typescript
...
const success = await axRobot.stopPlayAudio(1);
...
```

