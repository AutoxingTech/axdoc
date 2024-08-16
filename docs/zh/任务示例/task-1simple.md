# 简单任务示例

提供下以下一个最简单的到点A的示例

任务中播放背景音乐主要在当前点数据里设置本地音频动作实现，主要其实就是传入要到底点A的坐标，注释掉的都是可以不传入的

```typescript
  const task1 = {
    "name": "多点任务", 1, // 任务名称 不必须
    // "runMode": <runMode>, // 任务mode 不必须
    // "runNum": <runNum>, // 次数 不必须 默认1
    // "taskType": <taskType>, // 任务类型 不必须
    // "runType": <runType>, /// 运行模式 不必须
	pts: [
		 {
            "x": 6.7925255925160855, // A点的x坐标
            "y": 1.2596787664165277, // A点的y坐标
            // "yaw": 268, /// A点的yaw 不必须
            "areaId": "66879695c207ce62f87991c7", // A点的区域id
            // "dockingRadius": "1",
            // "ext": {
            //     "name": "点位一",
            //     "id": "668796861f783f4b11c89ddc"
            // },
            // "stepActs": [ // 动作
            //     {
            //         "type": 40
            //     },
            // ]
        }
	]
  }
  const success = axRobot.startTask(task1)

```
