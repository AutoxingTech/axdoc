# ActionData - InterAction

等待交互动作参数

## 属性

| 名称        | 数据类型 | 说明                               |
| ----------- | -------- | ---------------------------------- |
| `pauseTime` | number   | 暂停时间，单位：秒<br/>0表示不等待 |

## 示例

```typescript
{
  "type": ActionType.InterAction,
  "data": {
    "pauseTime": 20
  }
}
```

