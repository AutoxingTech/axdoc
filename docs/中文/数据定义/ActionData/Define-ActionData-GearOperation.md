# ActionData - GearOperation

喷雾器操作动作参数

## 属性

| 名称      | 数据类型 | 说明                                               |
| --------- | -------- | -------------------------------------------------- |
| `subType` | number   | 喷雾动作参数；<br/>0:关喷雾，1-5 设置档位,打开喷雾 |

## 示例

```typescript
{
  "type": ActionType.GearOperation,
  "data": {
    "subType": 2
  }
}
```

