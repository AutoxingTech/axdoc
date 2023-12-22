# ActionData - StopAudio

停止播放音频动作参数

## 属性

| 名称      | 数据类型 | 说明                                                         |
| --------- | -------- | ------------------------------------------------------------ |
| `mode`    | number   | 执行模式；<br/>1 - 上位机执行<br/>2 - 底盘执行               |
| `channel` | number   | 播放声道；<br/>1 - 普通音乐<br/>2 - 背景音乐<br/>底盘不支持多声道播放 |

## 示例

```typescript
{
  "type": ActionType.StopAudio,
  "data": {
    "mode": 1,
    "channel": 1
  }
}
```

### 