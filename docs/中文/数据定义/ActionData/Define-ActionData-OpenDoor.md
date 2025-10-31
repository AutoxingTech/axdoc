# ActionData - OpenDoor

打开箱门动作参数

## 属性

| 名称      | 数据类型 | 说明                                           |
| --------- | -------- | ---------------------------------------------- |
| `mode`    | number   | 执行模式；<br/>1 - 上位机执行<br/>2 - 底盘执行 |
| `doorIds` | number[] | 舱门编号；顺序从上到下从左到右依次为1,2,3,4    |

## 示例

```typescript
{
  "type": ActionType.OpenDoor,
  "data": {
    "mode": 1,
    "doorIds": [1]
  }
}
```

### 