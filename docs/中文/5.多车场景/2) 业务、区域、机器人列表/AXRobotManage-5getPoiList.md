# 获取所有站点

## `getPoiListExtend(req) -> {Promise.<any>}`

获取站点列表，之前获取站点必须传车，如果不传车会默认查询连接车辆的站点数据，现在扩展为可根据业务、区域、机器人随便组合查询条件都可查询对应站点数据。

### 参数

| 名称  | 数据类型                              | 说明     |
| ----- | ------------------------------------- | -------- |
| `req` | [RequestParam](../../8.数据定义/Define-RequestParam) | 请求参数 |

### 返回值 `Promise.<any>`

站点列表

### 示例

```typescript
...
const result = await getPoiListExtend({
  businessId: "<businessId>", // 可选（之一）
  areaId: "<areaId>", // 可选（之一）
  robotId: "<robotId>" // 可选（之一）
});

console.log(result.count); // 符合条件的 POI 总数量
console.log(result.list); // 站点列表
result.list.forEach(poi => {
  console.log(poi.areaId); // 站点所在区域的标识
  console.log(poi.buildingId); // 站点所在楼宇的标识
  console.log(poi.businessId); // 站点所属业务的标识
  console.log(poi.floor); // 站点所在楼层
  console.log(poi.id); // 站点标识
  console.log(poi.name); // 站点名称
  console.log(poi.type); // 站点类型
  console.log(poi.coordinates); // 站点坐标，格式为 [x, y]；如 [13.411045089526397,-6.95027412476179]
  console.log(poi.yaw); // 站点朝向角度值 单位：度
});
...
```

