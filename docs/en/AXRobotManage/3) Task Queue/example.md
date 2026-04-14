````markdown
# Queue Task Complete Example

### Initialization - Business Subscription - Create Task - Cancel Task - Task Details


```typescript
  import { AXRobotManage as AXRobot, AppMode } from "@autoxing/robot-js-sdk";
  // Create AXRobot instance
  this.axRobot = new AXRobotManage({
    "appId": "${appId}",
    "secret": "${secret}",
    "mode": AppMode.WAN_APP,
    "serverUrl": "${serverUrl}",
    "wsUrl": "${wsUrl}",
    "sourceType": 6
  })
  // Initialize AXRobot instance
  const success = await this.axRobot.init()
  console.log('success', success)
  // Connect business
  await this.axRobot.connectBusiness('${businessId}')
  // Subscribe to business
  await this.axRobot.subscribeRobotsStateByBus({
    onRobotListStatusChanged: state => {
      console.log('state', state)
    }
  })
  
  // Create task method
  async createQueueTask () {
      // robotId: Robot identifier for task execution, required for normal tasks; can be empty for queue tasks, but ensure there are robots under the businessId
      const taskObj = {
        "dispatchType": 2, // Task type 0 Normal task  2 Queue task
        "name": "Create task V3_" + new Date().getTime(),
        "businessId": "${businessId}", // Business identifier, required for queue tasks; can be empty for normal tasks
        // "robotId": "{robotSn}", // Robot identifier for task execution, required for normal tasks; can be empty for queue tasks, but ensure there are robots under the businessId
        "runNum": 1, // Execution count, default is 1, 0 means infinite loop
        "taskType": 4, // Task type 0 Disinfection 1 Return to charging station 2 Restaurant 3 Hotel 4 Delivery (5-in-1) 5 Factory 6 Chassis mini program 7 Charging scheduling
        "runType": 21, // Run type 0 Scheduled disinfection 1 Temporary disinfection 20 Quick delivery 21 Multi-point delivery 22 Direct 23 Cruise 24 Return 25 Charging station 26 Summon 27 Birthday mode 28 Guide 29 Lift 30 Lift cruise 31 Flexible transport 32 Roller 33 Full battery leave station
        "routeMode": 1, // Route mode, default is 1: 1 Sequential routing 2 Shortest distance routing
        "runMode": 1, // Driving mode, default is 1: 1 Flexible obstacle avoidance 2 Drive along track with small range obstacle avoidance 3 Drive along track without obstacle avoidance 4 Drive along track without rack docking point 5 Segmented routing
        "ignorePublicSite": true, // Whether to ignore public sites, default is not to ignore
        "speed": -1, // Robot driving speed, unit: m/s, recommended speed 0.4~1.0
        "sourceType": 6, // Task source type, must be 6 for secondary development
        "returnDest": 1, // Return setting  0 Invalid  1 According to robot settings  2 No return  3 Return to specified point, must set backPt  4 Idle return, must set backPt
        "returnTime": 5, // Idle duration, unit: seconds
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
                "name": "Floor 19 standby point",
                "id": "695a1dccfff76da93edbf6d8"
            }
        }
        
      }
      try {
        const res = await this.axRobot.createQueueTask(taskObj)
        this.taskId = res.taskId
        console.log('createQueueTask Success:', res)
        console.log('Current task id', this.taskId)
      } catch (error) {
        console.log('createQueueTask Error:', error)
      }
    }
    // Cancel task method
    async cancelQueueTaskById () {
      try {
        const res =await this.axRobot.cancelQueueTaskById(this.taskId)
        console.log('cancelQueueTaskById Success:', res)
      } catch (error) {
        console.log('cancelQueueTaskById Error:', error)
      }
    }
    // Get task details method
    async getQueueTaskDetails () {
      try {
        const res = await this.axRobot.getQueueTaskDetails(this.taskId)
        console.log('getQueueTaskDetails Success:', res)
      } catch (error) {
        console.log('getQueueTaskDetails Error:', error)
      }
    },

```



````
