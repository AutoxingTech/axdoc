# 获取有效区域列表

## `getEffectiveAreaList() -> {Promise.<any>}`

获取有效区域列表

### 参数

无

### 返回值 `Promise.<any>`

| 字段名称               | 类型   | 说明                                                                   |
| ---------------------- | ------ | ---------------------------------------------------------------------- |
| `status`               | number | 响应状态码<br />200 - 成功<br />400 - 参数错误<br />500 - 服务内部错误 |
| `message`              | string | 响应状态描述                                                           |
| `data`                 | object | 响应数据                                                               |
| `data.effective`       | array  | 有效区域列表 - 实际楼层                                                |
| `data.ineffective`     | array  | 无效区域列表 - 实际楼层                                                |
| `data.effectiveFloorNames`   | array  | 有效区域列表 - 显示楼层                                                |
| `data.ineffectiveFloorNames` | array  | 无效区域列表 - 显示楼层                                                |

```json
{
  "status": 200,
  "message": "ok",
  "data": {
    "effective": [-1, 1, 3],
    "ineffective": [-2, 2, 5, 6, 7],
    "effectiveName": [-1, 1, 3],
    "ineffectiveName": [-2, 2, 5, 6, 7]
  }
}
```

### 示例

```typescript
...
const result = await getEffectiveAreaList();
// todo someting
...
```
