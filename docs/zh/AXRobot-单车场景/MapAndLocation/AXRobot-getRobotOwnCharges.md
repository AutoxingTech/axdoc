# 获取机器人绑定的充电桩

## `getRobotOwnCharges() -> {Promise.<any>}`

获取机器人绑定的充电桩列表

### 参数

无

### 返回值 `Promise.<any>`

充电桩列表

### 示例

```typescript
...
const charges = await axRobot.getRobotOwnCharges();

console.log(charges.count); // 充电桩数量
console.log(charges.list); // 充电桩列表
charges.list.forEach(chargingPile => {
  console.log(chargingPile.areaId); // 充电桩所在区域的标识
  console.log(chargingPile.buildingId); // 充电桩所在楼宇的标识
  console.log(chargingPile.businessId); // 充电桩所属业务的标识
  console.log(chargingPile.floor); // 充电桩所在楼层
  console.log(chargingPile.id); // 充电桩标识
  console.log(chargingPile.name); // 充电桩名称
  console.log(chargingPile.coordinate); // 充电桩坐标，格式为 [x, y]；如 [13.411045089526397,-6.95027412476179]
  console.log(chargingPile.yaw); // 充电桩朝向角度值 单位：度
});
...
```

