# 订阅机器人状态

## `subscribeRealState(listener) -> {void}`

订阅机器人实时状态

### 参数

| 名称       | 数据类型                                   | 说明                   |
| ---------- | ------------------------------------------ | ---------------------- |
| `listener` | [OnRobotListner](../../8.数据定义/Define-OnRobotListener.md) | 机器人实时状态订阅回调 |

### 返回值

无

### 示例

```typescript
...
axRobot.subscribeRealState({
  onStateChanged: state => {
    // 常用
    console.log(state.isManualMode); // 是否推动模式
    console.log(state.isTasking); // 是否正在执行任务
    console.log(state.isCharging); // 是否正在充电
    console.log(state.isRemoteMode); // 是否远程控制
    console.log(state.battery); // 当前电量（百分比）
    console.log(state.robotId); // 机器人标识
    console.log(state.isFrontBumperPressed); // 检测到前方碰撞，机器人停止运动
    console.log(state.isRearBumperPressed); // 检测到后方碰撞，机器人停止运动
    console.log(state.isWaitingForDest); // 正在临停部位中，等待其他机器人离开
    console.log(state.speed); // 当前速度（m/s）
    console.log(state.areaId); // 当前区域ID
    console.log(state.isEmergencyStop); // 是否急停状态
    console.log(state.x); // 位置坐标的 x 分量
    console.log(state.y); // 位置坐标的 y 分量
    console.log(state.yaw); // 当前角度（弧度）
    console.log(state.locQuality); // 当前定位质量（0-100）
    console.log(state.hasObstruction); // 当前是否存在障碍物
    console.log(state.errors); // 故障码
    console.log(state.isGoHome); // 是否正在回桩充电中
    console.log(state.timestamp); // 机器人状态的时间戳
    // 不常用
    console.log(state.moveCreator); // 移动创建者
    console.log(state.stuckState); // 卡住状态[none: 没有卡住、move_stucked: 移动受阻、viewport_blocked: 视觉遮挡]
    console.log(state.moveState); // 移动状态[idle: 空闲、moving: 移动中、succeeded: 移动成功、cancelled: 移动被取消、failed: 移动失败]
    console.log(state.dispatch); // 调度状态[0: 非调度状态、3: 被调度]
    console.log(state.isOnLine); // 机器人在线状态  如果没有，说明当前sdk版本不支持
    console.log(state.enableRcs); // 机器人是否启用RCS  如果没有，说明当前sdk版本不支持
    console.log(state.isDeviceLocked); // 锁机；字段缺失：解锁  如果没有，说明当前sdk版本不支持
    console.log(state.voicePercent); // 音量调节区域  如果没有，说明当前sdk版本不支持
    // 顶升机器人
    console.log(state.jackProgress); // 顶升升起状态
    // 叉车机器人
    console.log(state.pushHandleMode); // 叉车行驶模式
    console.log(state.robotSignal); // 叉车转向状态
    // do something
  }
});
...
```

