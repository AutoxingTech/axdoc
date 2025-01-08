# 任务构造函数指引

提供任务的构造函数，需要者可以直接摘取用到自己项目里面。

构造函数

```typescript

export class TaskBuilder {
    public task: any
    constructor(name?: string, runNum?: number, taskType?: number, runType?: number) {
        this.task = {
            name: name,
            runNum: runNum ? runNum : 1,
            taskType: taskType ? taskType : 2,
            runType: runType? runType : 20,
            sourceType: 6,
            taskPts: []
        }
    } 
    /**
    * 添加点位数据
    * @returns
    */
    public addTaskPt(point: any): any {
        if (point) {
            this.task.taskPts.push(point)
        }
    }
}
export class TaskPoint {
    public taskPt: any
    /**
    * 点位数据转化
    * @returns
    */
    constructor(point: any) {
        if (point) {
            this.taskPt = {
                x: point.x ? point.x : (point.coordinate && point.coordinate.length > 0) ? point.coordinate[0] : '',
                y: point.y ? point.y : (point.coordinate && point.coordinate.length > 0) ? point.coordinate[1] : '',
                yaw: point.yaw,
                areaId: point.areaId,
                type: point.type,
                ext: {
                    name: point.name,
                    id: point.id
                },
                stepActs: []
            }
        } else {
            this.taskPt = null
        }
    }
    /**
    * 添加任务动作
    * @returns
    */
    public addStepActs(act: any): any {
        if (this.taskPt && act) {
            this.taskPt.stepActs.push(act)
        }        
    }
}
export class StepAction {
    /**
    * 播放音频
    * @returns
    */
    public PlayAudioAction(audioId: string): any {
        if (!audioId) {
            return false
        }
        return {
            "type": 5,
            "data": {
                "mode": 1,
                "url":"",
                "audioId": audioId,
                "interval": -1,
                "num": 1,
                "volume": 100,
                "channel": 1,
                "duration":-1,
            }
        }
    }
     /**
    * 关闭音频 type: 36
    * @returns
    */
     public CloseAudioAction(audioId: string): any {
        if (!audioId) {
            return false
        }
        return {
            "type": 36,
            "data": {
                "mode": 1,
                "url":"",
                "audioId": audioId,
                "interval": -1,
                "num": 1,
                "volume": 100,
                "channel": 1,
                "duration":-1,
            }
        }
    }
    /**
    * 目的地停留 type: 18
    * @returns
    */
    public PauseAction(duration: number): any {
        if (!duration && duration != 0) {
            return false
        }
        return {
            "type": 18,
            "data": {
                "pauseTime": duration
            }
        }
    }
    /**
    * 等待交互 type: 40
    * @returns
    */
    public WaitAction(duration?: number): any {
        let data = {
            "type": 40,
            "data": {
                "pauseTime": duration
            }
        }
        if (!duration && duration != 0) {
            delete data.data
        }
        return data
    }
    /**
    * 操作舱门 type: 6 开舱门 
    * @returns
    */
    public OpenDoor(doorIds: Array<string>): any {
        if (!doorIds || doorIds.length == 0) {
            return false
        }
        let data = {
            "type": 6,
            "data": {
                "mode": 2,
                "doorIds": doorIds
            }
        }
        return data
    }

    /**
    * 操作舱门  type: 28 关舱门  
    * @returns
    */
    public CloseDoor(doorIds: Array<string>): any {
        if (!doorIds || doorIds.length == 0) {
            return false
        }
        let data = {
            "type": 28,
            "data": {
                "mode": 2,
                "doorIds": doorIds
            }
        }
        return data
    }
}

```

利用上面构造函数创建任务

```typescript

    // 获取机器人所有点位数据
    const result = await axRobot.getPoiList({
        robotId: "<robotId>"
    });
    const poiList = result.list
    console.log('poiList', poiList)

    // 获取机器人某个点位
    if (poiList.length > 0) {
        let taskBuilder = new TaskBuilder('测试任务', 1, 2, 20)
        const stepAction = new StepAction()

        let pt1 = new TaskPoint(poiList[0])
        pt1.addStepActs(stepAction.WaitAction(20))
        pt1.addStepActs(stepAction.PlayAudioAction('<audioId>'))
        const taskPt1 = pt1.taskPt
        console.log('taskPt1', taskPt1)
        taskBuilder.addTaskPt(taskPt1)
        
        let pt2 = new TaskPoint(poiList[2])
        pt2.addStepActs(stepAction.WaitAction(3))
        pt2.addStepActs(stepAction.PlayAudioAction('<audioId>'))
        const taskPt2 = pt2.taskPt
        console.log('taskPt2', taskPt2)
        taskBuilder.addTaskPt(taskPt2)

        
        const task = taskBuilder.task
        console.log('task', task)
        // 发起任务
        const isOk = await axRobot.startTask(task)
        if (isOk) {
            console.log("任务发起成功")
        }
    }

```