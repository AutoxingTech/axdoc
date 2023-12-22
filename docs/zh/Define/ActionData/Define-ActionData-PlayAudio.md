# ActionData - PlayAudio

播放音频动作参数

## 属性

| 名称       | 数据类型 | 说明                                                         |
| ---------- | -------- | ------------------------------------------------------------ |
| `audioId`  | string   | 可选；<br/>本地音频资源标识，默认为文件名                    |
| `url`      | string   | 可选；<br/>音频在线 URL                                      |
| `volume`   | number   | 音量；0~100                                                  |
| `mode`     | number   | 执行模式；<br/>1 - 上位机执行<br/>2 - 底盘执行               |
| `interval` | number   | 循环播放间隔时间；单位：秒<br/>-1 表示只播放一次             |
| `num`      | number   | 可选；播放次数                                               |
| `duration` | number   | 可选；总播放时长；单位：秒<br/>如果同时设置了 `num` 参数则以 `num` 参数设置为准 |
| `channel`  | number   | 播放声道；<br/>1 - 普通音乐<br/>2 - 背景音乐<br/>底盘不支持多声道播放 |

## 示例

```typescript
{
  "type": ActionType.PlayAudio,
  "data": {
    "audioId": "3111001",
    "volume": 50,
    "mode": 1,
    "interval": 20,
    "num": 10,
    "channel": 1
  }
}
```

### 