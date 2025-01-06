# Example of areas Lifting Task

Example of lifting task for zone to zone: lifting shelf area A ->lifting shelf area B:
```typescript
const task4 = {
  "name": "task 1735886389655",
  "runNum": <runNum>,
  "taskType": <taskType>,
  "runType": <runType>,
  "routeMode": <routeMode>,
  "runMode": <runMode>,
  "ignorePublicSite": false,
  "sourceType": 6,
  "taskPts": [
    {
      "x": 6.1196619708425715, // one poi of area A x
      "y": 1.6438252919215302,// one poi of area A y
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "<areaId>",
      "type": -1,
      "ext": {
        "name": "A", // name of area A
        "id": "672d7001c26e184435add4d9" // id of area A
      },
      "stepActs": [
        {
          "type": 47, // Lifting action: Lift up
          "data": {
            "useAreaId": "672d7001c26e184435add4d9" // Use shelf area, required shelf area A ID
          }
        }
      ]
    },
    {
      "x": 12.491409954691335, // one poi of area B x
      "y": 1.3967850132701187, // one poi of area B x
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "<areaId>",
      "type": -1,
      "ext": {
        "name": "B", // name of area B
        "id": "672d705272c9edf34d02a6a5" // id of area B
      },
      "stepActs": [
        {
          "type": 48, // Lifting action: Lower down
          "data": {
            "useAreaId": "672d705272c9edf34d02a6a5" // Use shelf area, required shelf area B ID
          }
        }
      ]
    }
  ]
}
const success = axRobot.startTask(task4)
```