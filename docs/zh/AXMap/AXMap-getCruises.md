# 获取巡游路线

## `getCruises() -> {Promise<any>}`

获取巡游路线

### 参数

| 名称         | 类型   | 说明               |
| ------------ | ------ | ------------------ |
| `businessId` | string | 可选; 业务标识 |

### 返回值 `Promise.<any>`

| 名称      | 类型 | 说明     |
| --------- | ---- | -------- |
| `result` | any  | 巡游信息 |

### 示例

```typescript
...
const result = await axRobot.getCruises(cruiseInfo);
console.log(result.status)
console.log(result.data)
let cruise = result.data[0]
console.log(cruise.id)
console.log(cruise.name)
console.log(cruise.businessId)
console.log(cruise.sites)
...
```
