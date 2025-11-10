# ActionData - OpenLight

打开灯带动作参数动作参数

## 属性

| 名称     | 数据类型                          | 说明                                           |
| -------- | --------------------------------- | ---------------------------------------------- |
| `mode`   | number                            | 执行模式；<br/>1 - 上位机执行<br/>2 - 底盘执行 |
| `color`  | [LightColor](../Define-LightColor) | 灯带颜色                                       |
| `indexs` | [LightIndex](../Define-LightIndex) | 可选；分段显示，目前最多支持分4段              |

## 示例

```typescript
{
  "type": ActionType.OpenLight,
  "data": {
    "mode": 1,
    "color": LightColor.Green,
    "indexs": [
      {
        "index": 0,
        "num": 10
      }
    ]
  }
}
```