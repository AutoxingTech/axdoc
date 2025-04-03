# 转动角速度限速

## `setWeightSpeedLimit(args) -> {Promise.<boolean>}`

转动角速度限速
### 参数

| 名称     | 数据类型      | 说明  |
|--------|-----------|-----|
| `args` | {type: 0} |  0: disable; 1: enable  |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
axRobot.setWeightSpeedLimit({type: 1}); //启用转动角速度限速
...
```

