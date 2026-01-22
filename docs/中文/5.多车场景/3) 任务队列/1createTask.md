# 创建任务队列

## 方法

## `createQueueTask(taskObj) -> {Promise.<any>}`

根据业务id获取区域列表

### 参数

| 名称         | 类型    | 说明     |
| ------------ | -------| -------- |
| `taskObj` | string |  任务对象 |

taskObj

| 名称         | 类型    | 说明                                                                                                             |
| ------------ | -------|----------------------------------------------------------------------------------------------------------------|
| `name` | string | 任务名称(required)                                                                                                 |
| `businessId` | string | 业务标识，如果创建队列任务，则该字段必传；如果是普通任务，则该字段可以为空                                                                          |
| `robotId` | string | 执行任务的机器人标识，如果创建普通任务，则该字段必传；如果是队列任务，则该字段可以为空，但要保证 businessId 对应的业务下有机器人                                         |
| `dispatchType` | integer | 任务类型  2 队列任务                                                                                             |
| `runNum` | integer | 执行次数 默认为1,0表示无限循环                                                                                              |
| `taskType` | integer | 任务类型 0 消杀 1 回充电桩 2 餐厅 3 酒店 4 送物(五合一) 5 工厂 6 底盘小程序 7 充电调度                                                       |
| `runType` | integer | 运行类型 0 定时消杀 1 临时消杀 20 快捷送餐 21 多点送餐 22 直达 23 巡游 24 返航 25 充电桩26 召唤 27 生日模式 28 引领 29 顶升 30 顶升巡游31 灵活搬运32 辊筒33 满电离桩 |
| `routeMode` | integer | 行驶模式,默认为1 1 灵活躲避障碍 2 按轨迹行驶小范围避障 3 按轨迹行驶不避障 4 按轨迹行驶不补货架对接点 5分段算路                                                |
| `ignorePublicSite` | boolean | 是否忽略公共站点,默认是不忽略                                                                                                |
| `speed` | integer | 机器人行驶速度，单位：米/秒 建议速度 0.4~1.0                                                                                    |
| `sourceType` | integer | 任务来源类型 二开要求必须是6                                                                                                |
| `returnDest` | integer | 返航设置  0无效  1按车端设置  2不返航  3返航指定点，必须设置backPt  4空闲返航，必须设置backPt                                                   |
| `returnTime` | integer | 空闲时长，单位：秒  returnDest 为1  2 时不用传这个字段                                                                                              |
| `curPt` | object | 机器人当前位置                                                                                                        |
| `taskPts` | array | 任务点列表                                                                                                          |
| `backPt` | object | 返航点                                                                                                            |



### 返回值 `Promise.<any>`

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `taskId` | String        | 任务id         |



### 请求示例

```javascript
...

const taskObj = {
  "dispatchType": 2, // 任务类型  2 队列任务
  "name": "创建队列任务_" + new Date().getTime(),
  "businessId": "${businessId}", // 业务标识，如果创建队列任务，则该字段必传；如果是普通任务，则该字段可以为空
  // "robotId": "${robotSn}", // 执行任务的机器人标识，如果创建普通任务，则该字段必传；如果是队列任务，则该字段可以为空，但要保证 businessId 对应的业务下有机器人
  "runNum": 1, // 执行次数 默认为1,0表示无限循环
  "taskType": 4, // 任务类型 0 消杀 1 回充电桩 2 餐厅 3 酒店 4 送物(五合一) 5 工厂 6 底盘小程序 7 充电调度
  "runType": 21, // 运行类型 0 定时消杀 1 临时消杀 20 快捷送餐 21 多点送餐 22 直达 23 巡游 24 返航 25 充电桩26 召唤 27 生日模式 28 引领 29 顶升 30 顶升巡游31 灵活搬运32 辊筒33 满电离桩
  "routeMode": 1, // 算路模式,默认为1 1 顺序算路 2 最短距离算路
  "runMode": 1, // 行驶模式,默认为1 1 灵活躲避障碍 2 按轨迹行驶小范围避障 3 按轨迹行驶不避障 4 按轨迹行驶不补货架对接点 5分段算路
  "ignorePublicSite": true, // 是否忽略公共站点,默认是不忽略
  "speed": -1, // 机器人行驶速度，单位：米/秒 建议速度 0.4~1.0
  "sourceType": 6, // 任务来源类型 二开要求必须是6
  "returnDest": 1, // 返航设置  0无效  1按车端设置  2不返航  3返航指定点，必须设置backPt  4空闲返航，必须设置backPt
  "returnTime": 5, // 空闲时长，returnDest 为1  2 时不用传这个字段  单位：秒
  "curPt": {
      "stepActs": [
          {
              "type": 5,
              "data": {
                  "audioId": "3111501",
                  "interval": -1,
                  "mode": 1,
                  "playInBackground": true
              }
          }
      ]
  },
  "taskPts": [
      {
          "x": 5.106577288813696,
          "y": -14.983136481276915,
          "yaw": 95.59169811320771,
          "areaId": "695a1dd928359b42d68a5f0f",
          "type": -1,
          "ext": {
              "name": "19001",
              "id": "695a1dccfff76da93edbf6d4"
          },
          "stepActs": [
              {
                  "type": 5,
                  "data": {
                      "mode": 1,
                      "audioId": "3112056",
                      "interval": -1
                  }
              },
              {
                  "type": 18,
                  "data": {
                      "pauseTime": 5
                  }
              }
          ]
      }
  ],
  "backPt": {
      "x": 1.3910798196548058,
      "y": -24.785015864239313,
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "695a1dd928359b42d68a5f0f",
      "type": 10,
      "ext": {
          "name": "19层待命点",
          "id": "695a1dccfff76da93edbf6d8"
      }
  },
  
}
try {
  const res = await this.axRobot.createQueueTask(taskObj)
  this.taskId = res.taskId
  console.log('createQueueTask Success:', res)
  // createTaskV3 Success: {taskId: 'tsn-be48a330-6044-45cc-9756-a9ed7ff9d3d4'}
  console.log('当前任务id', this.taskId)
} catch (error) {
  console.log('createQueueTask Error:', error)
}
...
```

### 响应数据示例

```JSON
...
	{"taskId": "tsn-be48a330-6044-45cc-9756-a9ed7ff9d3d4"}
...
```


