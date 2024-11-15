# 设置机器人轮廓线

## `saveRobotFootprint(footprintInfo) -> {Promise.<boolean>}`

设置机器人轮廓线



### 参数

| 名称       | 类型     | 说明               |
| ---------- |--------|------------------|
| `footprintInfo`     | any | 机器人轮廓线集合 |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败


### 示例

```typescript
...
const success = await axRobot.saveRobotFootprint({footprint: [[0.248, 0.108], [0.24, 0.174], [0.231, 0.207], [0.211, 0.236], ...]});
console.log(success); // 机器人轮廓线设置是否成功
...
```

