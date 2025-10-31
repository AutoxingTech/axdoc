# 重新定位

## `resetPose(mapPose, isChargingPose) -> {Promise.<boolean>}`

重设机器人位姿

### 参数

| 名称             | 数据类型                    | 说明                   | 备注                                                                      |
| ---------------- | --------------------------- | ---------------------- | ------------------------------------------------------------------------- |
| `mapPose`        | [MapPose](../../../Define/Define-MapPose) | 位姿                   |                                                                           |
| `isChargingPose` | boolean                     | 可选；是否为充电桩位姿 | **默认为充电桩位姿** <br> **`false`: 机器人当前位姿, `true`: 充电桩位姿** |

### 返回值 `Promise.<boolean>`

设置是否成功

- `true` - 成功
- `false` - 失败

### 示例

```typescript
...
const success = await resetPose({
  areaId: "<areaId>",
  x: 0,
  y: 0,
  yaw: 0
}, false);
...
```
