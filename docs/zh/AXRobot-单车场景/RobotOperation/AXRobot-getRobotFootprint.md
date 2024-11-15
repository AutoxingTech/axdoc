# 获取机器人轮廓线

## `getRobotFootprint() -> {Promise.<any>}`

获取机器人轮廓线



### 返回值 `Promise.<any>`


| 名称   | 类型   | 说明                     |
| ------ | ------ | ------------------------ |
| `footprint` | Array | 机器人轮廓线集合 |


### 示例

```typescript
...
const footprintData = await axRobot.getRobotFootprint();
console.log(footprintData.footprint); // 机器人轮廓线集合
...
```

