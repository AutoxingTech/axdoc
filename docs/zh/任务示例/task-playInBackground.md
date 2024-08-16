# 任务中播放背景音乐

提供下以下场景的task示例：

任务中播放背景音乐主要在当前点数据里设置本地音频动作实现

```typescript
  const task1 = {
    ...
    "curPt": { // current point info (unnecessary)
      ...
	  stepActs: [
		{
			type: 5, //本地音频
			data: {
				"audioId": "...", //音频id 示例：3111501 必须
				"interval": -1, // 必须
				"mode": 2, // 播放模式 1：头壳播放 2：底盘播放 必须
				"playInBackground": true // 是否播放背景音乐 true：播放背景音乐 必须
			}
		}
	  ]
    },
    ...
  }
  const success = axRobot.startTask(task1)

```
