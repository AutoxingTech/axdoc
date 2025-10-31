# 删除巡游路线

## `deleteCruise(ids) -> {Promise<boolean>}`

删除巡游路线

### 参数

| 名称  | 类型     | 说明             |
| ----- | -------- | ---------------- |
| `ids` | number[] | 巡游路线标识集合 |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 示例

```typescript
...
const success = await axRobot.deleteCruise(ids); 
...
```
