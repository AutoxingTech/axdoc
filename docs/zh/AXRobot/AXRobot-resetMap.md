# 切换地图

## `resetMap(areaId) -> {Promise.<boolean>}`

重设机器人地图区域

### 参数

| 名称     | 数据类型 | 说明         |
| -------- | -------- | ------------ |
| `areaId` | string   | 地图区域标识 |

### 返回值 `Promise.<boolean>`

设置是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
const success = await axRobot.resetMap("<areaId>");
...
```

