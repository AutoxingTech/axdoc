# PlayAudio

播放音频

## 属性

| 名称       | 数据类型 | 说明                                        |
| ---------- | -------- | ------------------------------------------- |
| `mode`     | number   | 1: 上位机处理, 2: 底盘处理                  |
| `url`      | string   | 音频地址                                    |
| `audioId`  | string   | 本地音频资源 ID                             |
| `volume`   | number   | 音量,取值 0-100                             |
| `interval` | number   | 循环播报间隔时间,单位:秒，-1 表示只播报一次 |
| `num`      | number   | 总播放次数                                  |
| `duration` | number   | 总播放时长,单位:秒                          |
