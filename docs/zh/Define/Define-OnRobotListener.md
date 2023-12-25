# OnRobotListener

机器人状态订阅回调

## 属性

| 名称            | 数据类型 | 说明               |
| --------------- | -------- | ------------------ |
| `onStateChange` | function | 机器人状态变化回调 |


## 参数

```javascript
StateInfo {
    x: number,
    y: number,
    yaw: number,
    isEmergencyStop: boolean,
    isManualMode: boolean,
    isTasking: boolean,
    isCharging: boolean,
    isRemoteMode: boolean,
    battery: number,
    robotId: string,
    speed: number,
    areaId: string,
    locQuality: number,
    hasObstruction: boolean,
    errors: Array<number>,
    chassisErrors: Array<number>,
    isGoHome: boolean,
    timestamp: number,
    vers?: { softVer?: string, hwVer?: string, seralVer?: string },
    moveState?: string,
    taskObj?: any,
    cancelTaskId?: string,
    dispatch: number,
    moveCreator?: string,
    stuckState?: string
}
```