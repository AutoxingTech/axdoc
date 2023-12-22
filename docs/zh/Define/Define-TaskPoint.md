# TaskPoint

任务节点信息

## 属性

| 名称         | 数据类型                         | 说明                         |
| ------------ | -------------------------------- | ---------------------------- |
| `areaId`   | string                           | 任务节点所在地图区域标识     |
| `x`        | number                           | 任务节点坐标 x 分量          |
| `y`        | number                           | 任务节点坐标 y 分量          |
| `yaw`      | number                           | 任务节点朝向；单位：角度     |
| `type`     | number                           | POI 类型；参考 [POI Type](../../Define/Define-PoiType) |
| `ext`      | object                           | 可选；任务节点自定义扩展信息 |
| `stepActs` | [BaseAction](../../Define/Define-BaseAction)[] | 可选；任务节点动作列表       |

## 示例

```json
{
  "x": 0.11,
  "y": 1.22,
  "yaw": 89,
  "areaId": "xxxx",
  "type": -1,
  "ext": {...},
  "stepActs": [...]
}
```
