# 获取机器人区域

## `getAreaList() -> {Promise.<any>}`

获取区域列表

### 参数

无

### 返回值 `Promise.<any>`

区域列表

### 示例

```typescript
...
const result = await axRobot.getAreaList();

const data = result.data
console.log(data.count); // 地图区域数量
console.log(data.list); // 地图区域列表
data.list.forEach(area => {
  console.log(area.id); // 区域标识
  console.log(area.buildingId); // 区域所属楼宇标识
  console.log(area.businessId); // 区域所属业务标识
  console.log(area.name); // 区域名称
  console.log(area.floor); // 区域在楼层
  console.log(area.createTime); // 区域创建时间
});
...
```

