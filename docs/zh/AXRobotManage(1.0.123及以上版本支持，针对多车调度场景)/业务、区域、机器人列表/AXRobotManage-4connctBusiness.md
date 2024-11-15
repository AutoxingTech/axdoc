# 连接业务

## 方法

## `connectBusiness(businessId, areaId) -> {void}`

连接当前业务。

### 参数

| 名称               | 类型                       | 说明     | 必须     |
| ------------------ | ----------------------- | -------- |-------- |
| `businessId`       | string |  业务标识 | 必须 |
| `areaId`           | string |  区域标识 | 不必须 |


### 请求示例

```javascript
...
await axRobot.connectBusiness('<businessId>', '<areaId>') 
...
```

