# OnRobotListener

Robot status subscription callback

## Attributes

| Name | Data Type | Description |
| --------------- | -------- | ------------------ |
| `onStateChange` | function | Robot state change callback |

### Parameters

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