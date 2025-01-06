# 区对区举升任务示例

区对区举升任务示例 货架区A举起  -> 货架区B举起  ：
```typescript
const task4 = {
  "name": "灵活搬运 1735886389655",
  "runNum": <runNum>,
  "taskType": <taskType>,
  "runType": <runType>,
  "routeMode": <routeMode>,
  "runMode": <runMode>,
  "ignorePublicSite": false,
  "sourceType": 6,
  "taskPts": [
    {
      "x": 6.1196619708425715, // 货架区A内的一个点 x
      "y": 1.6438252919215302,// 货架区A内的一个点 y
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "<地图id>",
      "type": -1,
      "ext": {
        "name": "A", // 货架区A名字
        "id": "672d7001c26e184435add4d9" // 货架区A id
      },
      "stepActs": [
        {
          "type": 47, // 举升动作 ： 举起
          "data": {
            "useAreaId": "672d7001c26e184435add4d9" // 使用货架区 ，必填 货架区A id
          }
        }
      ]
    },
    {
      "x": 12.491409954691335, // 货架区B内的一个点 x
      "y": 1.3967850132701187, // 货架区B内的一个点 x
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "<地图id>",
      "type": -1,
      "ext": {
        "name": "B", // 货架区B名字
        "id": "672d705272c9edf34d02a6a5" // 货架区B id
      },
      "stepActs": [
        {
          "type": 48, // 举升动作 ： 放下
          "data": {
            "useAreaId": "672d705272c9edf34d02a6a5" // 使用货架区 ，必填 货架区B id
          }
        }
      ]
    }
  ]
}
const success = axRobot.startTask(task4)
```