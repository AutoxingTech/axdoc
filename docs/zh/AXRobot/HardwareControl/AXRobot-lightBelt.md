# 灯带控制

## 方法

## `openLightBelt(lightBelt) → {Promise.<boolean>}`

打开灯带

### 参数

| 名称        | 类型                            | 说明 |
| ----------- | ------------------------------- | ---- |
| `lightBelt` | [LightBelt](../../../Define/Define-LightBelt) | 档位 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
let lightBelt = {
  mode: 1,
  color: LightColor.Green,
  indexs: [
    { index: 0, num: 6 }
  ]
}
const success = await axRobot.openLightBelt(lightBelt);
...
```



## `closeLightBelt(lightBelt) → {Promise.<boolean>}`

关闭灯带
### 参数

| 名称        | 类型                            | 说明 |
| ----------- | ------------------------------- | ---- |
| `lightBelt` | [LightBelt](../../../Define/Define-LightBelt) | 档位 |
### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
let lightBelt = {
	mode: 1,
  color: LightColor.Green,
	indexs: [
    { index: 0, num: 6 }
  ]
}
const success = await axRobot.closeLightBelt(lightBelt);
...
```

