# 创建任务

## 方法

## `createTask(task) -> {Promise.<string>}`

创建任务。



### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `task` | [TaskInfo](../../8.数据定义/Define-TaskInfo.md) | 任务信息 |



### 返回值 `Promise.<string>`

taskID


???+ WARNING "WARNING"
    创建任务并返回任务ID，需注意此时任务并未开始执行

### 示例




???+ Example "Example"
    任务描述：
        创建了一个多点送餐任务，到达餐桌A点并打开灯带，然后到达餐桌B并关闭灯带，完成后返回充电桩。

    ```javascript
    ...

    task = {
        "name": "多点送餐",
        "robotId": "xxxxxxx",
        "routeMode": 1, //1按任务点顺序算路,2按最短路径算路 默认为1
        "runMode": 1, //行驶模式 1 灵活躲避障碍 2 按轨迹行驶  默认为1
        "runNum": 1, //任务执行次数，默认为1，0表示无限循环
        "taskType": 2, //可选参数，默认为-1，任务类型 0 消杀 1回充电桩 2 餐厅 3 酒店 4 送物(五合一) 5 工厂 6 底盘小程序
        "runType": 21, //可选参数，默认为-1  运行类型  0 定时消杀 1 临时消杀  20 快捷送餐 21 多点送餐 22 直达 23 巡游 24 返航 25 回桩 26召唤 27餐厅生日模式任务 28引领 29顶升任务
        "ignorePublicSite": false, //是否忽略公共站点,默认是不忽略
        "pts": [{
                "x": -3.8,
                "y": 1.15,
                "yaw": 89,
                "areaId": "xxxxxx",
                "type": -1,
                "ext": {
                    "name": "餐桌A"
                },
                "stepActs": [{
                    "type": 37,
                    "data": {
                        "mode": 1, //执行模式，1 上位机执行  2 底盘执行
                        "color": 1,
                        "feature": 1,
                        "indexs": [{
                                "index": 0,
                                "num": 10
                            },
                            {
                                "index": 11,
                                "num": 10
                            }
                        ]
                    }
                }]
            },
            {
                "x": -0.45,
                "y": 0.55,
                "yaw": 89,
                "areaId": "xxxxxxxxxxx",
                "type": -1,
                "ext": {
                    "name": "餐桌B"
                },
                "stepActs": [{
                    "type": 38,
                    "data": {
                        "mode": 1, //执行模式，1 上位机执行  2 底盘执行
                        "indexs": [{
                                "index": 0,
                                "num": 10
                            },
                            {
                                "index": 11,
                                "num": 10
                            }
                        ]
                    }
                }]
            }
        ],
        "backPt": {
            "type": 9, //点位类型，9充电桩 10待命点
            "x": 0.11,
            "y": 1.22,
            "yaw": 89,
            "stopRadius": 1, //停靠半径,单位:米，默认为1
            "areaId": "xxxx",
            "ext": {
                "name": "充电桩"
            }
        }
    }


    let taskId = await this.axRobot.createTask(task)


    ...
    ```



