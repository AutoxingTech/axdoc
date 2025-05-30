# Get Task Details

## Method

## `getTaskDetailsById(taskId) -> {Promise.<any>}`

Fetches the task details.。



### Parameters

| Name   | Type                          | Description     |
| ------ | ----------------------------- | -------- |
| `taskId` | string | Task identifier |



### Returns `Promise.<any>`
| Name         | Type                          | Description     |
|------------| ----------------------------- | -------- |
| `taskInfo` | [TaskInfo](../../../Define/Define-TaskInfo) | Task information |


### Example




???+ Example "Example"
    Retrieve task details by Task ID.

    ```javascript
    ...

    let taskInfo = await this.axRobot.getTaskDetailsById(taskId)

    taskInfo = {
        "name": "Multi-Point Delivery",
        "taskId": "xxxxxxxxxx",
        "businessId": "xxxxxxxxxx", // Business ID
        "speed": 0.8, // Speed
        "isCancel": false,
        "isFinish": true,
        "isExcute": true,
        "robotId": "xxxxxxx",
        "routeMode": 1, //1 Route by task point order, 2 Route by shortest path, default is 1
        "runMode": 1, //Driving mode 1 Flexible obstacle avoidance 2 Trajectory driving, default is 1
        "runNum": 1, //Number of task executions, default is 1; 0 means infinite loop
        "taskType": 2, //Optional parameter, default is -1; Task type 0 Disinfection 1 Return to charging station 2 Restaurant 3 Hotel 4 Delivery (Five-in-One) 5 Factory 6 Base application
        "runType": 21, //Optional parameter, default is -1; Run type 0 Timed disinfection 1 Temporary disinfection 20 Quick delivery 21 Multi-point delivery 22 Direct 23 Patrol 24 Return 25 Charging station 26 Call 27 Restaurant birthday mode task 28 Guide 29 Lifting task
        "ignorePublicSite": false, //Whether to ignore public sites, default is false
        "taskPts": [
            {
                "x": -3.8,
                "y": 1.15,
                "yaw": 89,
                "areaId": "xxxxxx",
                "type": -1,
                "ext": {
                    "name": "Table A"
                },
                "stepActs": [
                    {
                        "type": 37,
                        "data": {
                            "mode": 1, //Execution mode: 1 Upper control, 2 Chassis control
                            "color": 1,
                            "feature": 1,
                            "indexs": [
                                {
                                    "index": 0,
                                    "num": 10
                                },
                                {
                                    "index": 11,
                                    "num": 10
                                }
                            ]
                        }
                    }
                ]
            },
            {
                "x": -0.45,
                "y": 0.55,
                "yaw": 89,
                "areaId": "xxxxxxxxxxx",
                "type": -1,
                "ext": {
                    "name": "Table B"
                },
                "stepActs": [
                    {
                        "type": 38,
                        "data": {
                            "mode": 1, //Execution mode: 1 Upper control, 2 Chassis control
                            "indexs": [
                                {
                                    "index": 0,
                                    "num": 10
                                },
                                {
                                    "index": 11,
                                    "num": 10
                                }
                            ]
                        }
                    }
                ]
            }
        ],
        "backPt": {
            "type": 9, //Point type: 9 Charging station, 10 Standby point
            "x": 0.11,
            "y": 1.22,
            "yaw": 89,
            "stopRadius": 1, //Docking radius in meters, default is 1
            "areaId": "xxxx",
            "ext": {
                "name": "Charging station"
            }
        },
        "createTime":1724642946826,
        "isDel":false,
        "taskState":"success",
        "creatorName":"xxx",
        "taskLogs":[
            {
                "_id":"66cbf685ba27fc04fcfead82",
                "taskType":"transport",
                "logType":"event",
                "logName":"turn-on-light",
                "Data":{},
                "timestamp":1724642947292,
                "createTime":1724642949681
             },
        ],
        "taskTracks": {
            "65487c0dbaeab6a16e887dd5":[
                {
                    "timestamp":1724642947310,
                    "x":94.4,
                    "y":-14.4,
                    "yaw":1.5
                },
            ]
        }
    
    }



    ...
    ```



