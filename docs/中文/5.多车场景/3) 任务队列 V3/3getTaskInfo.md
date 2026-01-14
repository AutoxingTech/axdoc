# 获取任务详情

## 方法

## `getTaskInfoV3(taskId) -> {Promise.<any>}`

根据业务id获取区域列表

### 参数

| 名称         | 类型    | 说明     |
| ------------ | -------| -------- |
| `taskId` | string |  任务Id |

### 返回值 `Promise.<any>`

未执行任务：

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `name` | string |  任务名称(required) |
| `businessId` | string |  业务标识，如果创建队列任务，则该字段必传；如果是普通任务，则该字段可以为空 |
| `robotId` | string |  执行任务的机器人标识，如果创建普通任务，则该字段必传；如果是队列任务，则该字段可以为空，但要保证 businessId 对应的业务下有机器人 |
| `dispatchType` | integer |  任务类型 0 普通任务  2 队列任务 |
| `runNum` | integer |  执行次数 默认为1,0表示无限循环 |
| `taskType` | integer |  任务类型 0 消杀 1 回充电桩 2 餐厅 3 酒店 4 送物(五合一) 5 工厂 6 底盘小程序 7 充电调度 |
| `runType` | integer |   运行类型 0 定时消杀 1 临时消杀 20 快捷送餐 21 多点送餐 22 直达 23 巡游 24 返航 25 充电桩26 召唤 27 生日模式 28 引领 29 顶升 30 顶升巡游31 灵活搬运32 辊筒33 满电离桩 |
| `routeMode` | integer |  行驶模式,默认为1 1 灵活躲避障碍 2 按轨迹行驶小范围避障 3 按轨迹行驶不避障 4 按轨迹行驶不补货架对接点 5分段算路 |
| `ignorePublicSite` | boolean | 是否忽略公共站点,默认是不忽略 |
| `speed` | integer |   机器人行驶速度，单位：米/秒 建议速度 0.4~1.0 |
| `sourceType` | integer |  任务来源类型 二开要求必须是6 |
| `curPt` | object |  机器人当前位置  |
| `taskPts` | array |  任务点列表 |
| `backPt` | object |  返航点 |


执行任务：


| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `taskInfo` | [TaskInfo](../../8.数据定义/Define-TaskInfo.md) | 任务信息 |



### 请求示例

```javascript
...
try {
  const res = await this.axRobot.getTaskInfoV3(this.taskId)
  console.log('getTaskInfoV3 Success:', res)
} catch (error) {
  console.log('getTaskInfoV3 Error:', error)
}
...
```

### 响应数据示例

```JSON
...
  未执行:
	{
    "name": "创建任务V3_1767691318183",
    "taskId": "tsn-a56c4cb5-e0c7-463a-aa36-b35e6d5d68f2",
    "runType": 21,
    "taskType": 4,
    "businessId": "6930fdc2e5a9845a0e13c3e4",
    "robotId": "2152507706093Ah",
    "runNum": 1,
    "runMode": 1,
    "taskPts": [
        {
            "stepActs": [
                {
                    "type": 5,
                    "data": {
                        "audioId": "3112056",
                        "interval": -1,
                        "mode": 1
                    }
                },
                {
                    "type": 18,
                    "data": {
                        "pauseTime": 5
                    }
                }
            ],
            "ext": {
                "id": "695a1dccfff76da93edbf6d4",
                "name": "19001"
            },
            "areaId": "695a1dd928359b42d68a5f0f",
            "x": 5.106577288813696,
            "y": -14.983136481276915,
            "yaw": 95.59169811320773,
            "type": -1,
            "key": ""
        }
    ],
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
        ],
        "ext": null,
        "areaId": "",
        "key": ""
    },
    "backPt": {
        "ext": {
            "id": "695a1dccfff76da93edbf6d8",
            "name": "19层待命点"
        },
        "areaId": "695a1dd928359b42d68a5f0f",
        "x": 1.3910798196548058,
        "y": -24.785015864239313,
        "yaw": 0,
        "type": 10,
        "key": "",
        "stopRadius": 1
    },
    "createTime": 0,
    "updateTime": 0,
    "routeMode": 1,
    "speed": -1,
    "routeData": null,
    "ignorePublicSite": true,
    "dispatchType": 2,
    "ext": null,
    "sourceType": 6,
    "poiIdList": null,
    "poiTypeAudioList": null,
    "queueWeight": 7691317681000,
    "issueTime": 1767691318172
  }
  已执行：
  {
    "taskId": "tsn-75321169-a539-4ca2-bc8d-4964be35dff9",
    "name": "创建任务V3_1767691519690",
    "taskPts": [
        {
            "areaId": "695a1dd928359b42d68a5f0f",
            "ext": {
                "id": "695a1dccfff76da93edbf6d4",
                "name": "19001"
            },
            "key": "",
            "stepActs": [
                {
                    "data": {
                        "audioId": "3112056",
                        "interval": -1,
                        "mode": 1
                    },
                    "type": 5
                },
                {
                    "data": {
                        "pauseTime": 5
                    },
                    "type": 18
                }
            ],
            "type": -1,
            "x": 5.106577288813696,
            "y": -14.983136481276915,
            "yaw": 95.59169811320773
        }
    ],
    "runType": 21,
    "businessId": "6930fdc2e5a9845a0e13c3e4",
    "backPt": {
        "areaId": "695a1dd928359b42d68a5f0f",
        "ext": {
            "id": "695a1dccfff76da93edbf6d8",
            "name": "19层待命点"
        },
        "key": "",
        "stopRadius": 1,
        "type": 10,
        "x": 1.3910798196548058,
        "y": -24.785015864239313,
        "yaw": 0
    },
    "speed": -1,
    "taskType": 4,
    "runNum": 1,
    "busiType": 5,
    "ignorePublicSite": true,
    "isCancel": false,
    "isFinish": false,
    "robotId": "8981307a02163yT",
    "robotName": "63yT",
    "runMode": 1,
    "buildingId": "66da6f298fded280e731af7a",
    "isExcute": true,
    "createTime": 1767691519203,
    "routeMode": 1,
    "isDel": false,
    "taskLogs": [
        {
            "_id": "695cd501e02ff46ab8eb17e1",
            "taskType": "transport",
            "logType": "state",
            "logName": "task-start",
            "Data": {},
            "timestamp": 1767691520919,
            "createTime": 1767691521891
        },
        {
            "_id": "695cd501e02ff46ab8eb17e2",
            "taskType": "transport",
            "logType": "event",
            "logName": "play-audio",
            "Data": {},
            "timestamp": 1767691520964,
            "createTime": 1767691521898
        },
        {
            "_id": "695cd501e02ff46ab8eb17e3",
            "taskType": "transport",
            "logType": "state",
            "logName": "task-received",
            "Data": {},
            "timestamp": 1767691521406,
            "createTime": 1767691521909
        },
        {
            "_id": "695cd518e02ff46ab8eb17e5",
            "taskType": "transport",
            "logType": "state",
            "logName": "task-issue",
            "Data": {},
            "timestamp": 1767691520927,
            "createTime": 1767691544684
        },
        {
            "_id": "695cd518e02ff46ab8eb17e6",
            "taskType": "transport",
            "logType": "state",
            "logName": "task-received",
            "Data": {},
            "timestamp": 1767691520939,
            "createTime": 1767691544692
        }
    ],
    "taskTracks": {
        "695a1dd928359b42d68a5f0f": [
            {
                "timestamp": 1767691520976,
                "x": 1.475,
                "y": -23.7025,
                "yaw": 0.38
            },
            {
                "timestamp": 1767691520982,
                "x": 1.475,
                "y": -23.7025,
                "yaw": 0.38
            },
            {
                "timestamp": 1767691522010,
                "x": 1.475,
                "y": -23.7025,
                "yaw": 0.38
            },
            {
                "timestamp": 1767691528742,
                "x": 1.475,
                "y": -23.7025,
                "yaw": 0.38
            },
            {
                "timestamp": 1767691529802,
                "x": 1.5,
                "y": -23.7,
                "yaw": 0.51
            },
            {
                "timestamp": 1767691530875,
                "x": 1.56,
                "y": -23.65,
                "yaw": 0.77
            },
            {
                "timestamp": 1767691531938,
                "x": 1.73,
                "y": -23.375,
                "yaw": 1.16
            },
            {
                "timestamp": 1767691532992,
                "x": 1.8125,
                "y": -22.9325,
                "yaw": 1.39
            },
            {
                "timestamp": 1767691534044,
                "x": 1.92,
                "y": -22.72,
                "yaw": 0.51
            },
            {
                "timestamp": 1767691535100,
                "x": 2.18,
                "y": -22.6675,
                "yaw": -0.06
            },
            {
                "timestamp": 1767691536156,
                "x": 2.4675,
                "y": -22.655,
                "yaw": 0.12
            },
            {
                "timestamp": 1767691537206,
                "x": 2.64,
                "y": -22.615,
                "yaw": 0.32
            },
            {
                "timestamp": 1767691538286,
                "x": 2.7175,
                "y": -22.5925,
                "yaw": 0.24
            },
            {
                "timestamp": 1767691539336,
                "x": 2.7975,
                "y": -22.5625,
                "yaw": 0.16
            },
            {
                "timestamp": 1767691540388,
                "x": 2.85,
                "y": -22.555,
                "yaw": 0.13
            },
            {
                "timestamp": 1767691541448,
                "x": 2.9275,
                "y": -22.5425,
                "yaw": 0.18
            },
            {
                "timestamp": 1767691542499,
                "x": 2.9625,
                "y": -22.5325,
                "yaw": 0.3
            },
            {
                "timestamp": 1767691543561,
                "x": 2.93,
                "y": -22.5525,
                "yaw": 0.57
            },
            {
                "timestamp": 1767691544590,
                "x": 2.93,
                "y": -22.555,
                "yaw": 0.56
            },
            {
                "timestamp": 1767691545605,
                "x": 2.93,
                "y": -22.555,
                "yaw": 0.56
            },
            {
                "timestamp": 1767691551086,
                "x": 2.9225,
                "y": -22.5575,
                "yaw": 0.56
            }
        ]
    },
    "taskState": "running",
    "useTime": 30104,
    "creatorName": "",
    "mileage": 2.21,
    "sourceType": 6,
    "curPt": {
        "areaId": "",
        "key": "",
        "stepActs": [
            {
                "data": {
                    "audioId": "3111501",
                    "interval": -1,
                    "mode": 1,
                    "playInBackground": true
                },
                "type": 5
            }
        ],
        "type": 0,
        "x": 0,
        "y": 0
    }
  }
...
```


