# 多点任务到达后暂停等待交互示例（全）

多点任务到达后暂停等待交互：
```typescript
const task4 = {
    "name": "多点任务",
    "runMode": <runMode>,
    "runNum": <runNum>,
    "taskType": <taskType>,
    "runType": <runType>,
    "curPt": {},
    "pts": [
        {
            "x": 6.7925255925160855,
            "y": 1.2596787664165277,
            "yaw": 268,
            "areaId": "66879695c207ce62f87991c7",
            "dockingRadius": "1",
            "ext": {
                "name": "点位一",
                "id": "668796861f783f4b11c89ddc"
            },
            "stepActs": [
                {
                    "type": 40
                },
            ]
        },
        {
            "x": 9.005738806990848,
            "y": 1.2387888340015252,
            "yaw": 268,
            "areaId": "66879695c207ce62f87991c7",
            "dockingRadius": "1",
            "ext": {
                "name": "点位二",
                "id": "668796861f783f4b11c89dde"
            },
            "stepActs": [
                {
                    "type": 40
                },
            ]
        }
    ],
    "backPt": {},
    "ignorePublicSite": true,
    "ext": {
        "checkItems": [
            "elevator"
        ]
    },
    "soureceType": 1,
    "detourRadius": 1
}
const success = axRobot.startTask(task4)
```