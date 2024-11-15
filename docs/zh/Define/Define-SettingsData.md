# SettingsData

机器人设置参数

## 属性

| 名称        | 数据类型 | 说明              |
| ---------- | -------- | ----------------- |
| `basic`     | basicInfo     | 基本信息|
| `delivery`  | deliveryInfo   | 部署信息|
| `moderate`   | float   | 颠簸减速阈值 （0 - 1.0）|
| `moderateSwitch` | boolean   | 颠簸减速开关|
| `playLanguage` | number   | 播放语言|
| `runMode`   | number   | 运行模式 1：灵活避障； 2： 沿轨道行驶； 3：严格沿轨道行驶|
| `skipPtDelay`   | number   | 跳点延时 |
| `skipPtMode`   | number   | 跳点模式 1：打开 2：关闭|
| `sound`   | soundInfo   | 声音设置|
| `voicePercent`   |  number  | 音量 （0 - 100）|


basicInfo：

| 名称    | 数据类型 | 说明              |
| ------- | -------- | ----------------- |
| `char`     | string   | 默认充电桩:点位id   |
| `standby`  | string   | 默认返航点:点位id|

deliveryInfo：

| 名称    | 数据类型 | 说明              |
| ------- | -------- | ----------------- |
| `runSpeed`     | string   | 行驶速度   |

soundInfo:

| 名称    | 数据类型 | 说明              |
| ------- | -------- | ----------------- |
| `avoidVolume`     | number   | 音量 （0 - 100）  |