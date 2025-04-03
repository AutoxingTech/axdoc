# 获取区域图片

## `getAreaPic(areaId) -> {Promise.<any>}`

获取区域地图图片

### 参数

| 名称     | 数据类型 | 说明     |
| -------- | -------- | -------- |
| `areaId` | string   | 区域标识 |

### 返回值 `Promise.<any>`

区域地图图片数据流

### 示例

```typescript
...
const mapData = await axRobot.getAreaPic("<areaId>");
...
```

