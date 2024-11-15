# 获取指定机器人设置

## 方法

## `getRobotSettingById(robotId) -> {Promise.<any>}`

根据机器人id获取设置

### 参数

| 名称      | 类型                           | 说明     |
| --------- | ----------------------------- | -------- |
| `robotId` | string                        | 机器人标识 |



???+ 环境响应 

    === "云端"
        ## 返回值 `Promise.<any>`

          | 名称      | 类型                           | 说明     |
          | --------- | ----------------------------- | -------- |
          | `businessId` | string                     | 业务标识 |
          | `buildingId` | string                     | 建筑标识 |
          | `customSetting` | string                  | 设置数据 |

        ## 请求示例

          ```javascript
          ...
          let settingsData = {}
          const settingsResult = await axRobot.getRobotSettingById(robotId);
          if (settingsResult) {
            settingsData = settingsResult.customSetting;
          }
          ...
          ```
        ## 响应数据示例

          ```JSON
          ...
          {
            "businessId": "66432c72db3008878c5dd83c",
            "buildingId": "60a4c374059acc6c8bdff074",
            "customSetting": {
                "_id": "65b0da744242e2e435a7cbf2",
                "adjustSpray": 1,
                "areaId": "test_wyz",
                "basic": {
                    "char": "6643352e7fe5260984536181",
                    "standby": "6643352ea3f5a3ca0463968f"
                },
                "buildingId": "60a4c374059acc6c8bdff074",
                "businessId": "655aa633c5221eaa1181fedd",
                "carId": "B782401202631Gr",
                "createTime": 1706089076693,
                "customVoice": [],
                "delivery": {
                    "runSpeed": 72
                },
                "disinfectMode": 1,
                "gearMode": 2,
                "gearType": 2,
                "pauseTime": 0,
                "playLanguage": 2,
                "routeIds": [],
                "routeMode": 1,
                "runNum": 0,
                "settings": {},
                "skipPtMode": 2,
                "sound": {
                    "avoidVolume": 100
                },
                "speedMode": 2,
                "sprayMode": 1,
                "taskId": "47c482de-cf61-420f-8ce4-ed50bcff4b40",
                "taskName": "一键任务",
                "updateTime": 1716281269568,
                "voiceMode": 5,
                "voicePercent": 60
              }
          ...
          ```
    === "本地"
        ## 返回值 `Promise.<any>`
        
          | 名称            | 类型                     | 说明     |
          | --------------- | ------------------------ | -------- |
          | `robotId`       | string                   | 机器人标识 |
          | `businessScene` | string                   | 业务场景 |
          | `settings`      | string                   | 设置数据 |

        ## 示例

          ```javascript
          ...
          let settingsData = {}
          const settingsResult = await axRobot.getRobotSettingById(robotId);
          if (settingsResult) {
            settingsData = settingsResult.settings;
          }
          ...
          ```
        ## 响应数据示例

          ```JSON
          ...
          {
            "id": 1,
            "robotId": "81822013000931v",
            "businessScene": 2,
            "settings": {
              "animation": {
                "fhAnimation": {
                  "data": {
                    "id": "/storage/emulated/0/launcher/local/animation/감사합니다.gif",
                    "name": "감사합니다.gif",
                    "path": "/storage/emulated/0/launcher/local/animation/감사합니다.gif"
                  },
                  "switch": false
                },
                "scAnimation": {
                  "data": {
                    "id": "/storage/emulated/0/launcher/local/animation/감사합니다.gif",
                    "name": "감사합니다.gif",
                    "path": "/storage/emulated/0/launcher/local/animation/감사합니다.gif"
                  },
                  "switch": false
                },
                "sleepAnimation": {
                  "data": {
                    "id": "/storage/emulated/0/launcher/local/animation/化妆.gif",
                    "name": "化妆.gif",
                    "path": "/storage/emulated/0/launcher/local/animation/化妆.gif"
                  },
                  "switch": 0
                },
                "xyAnimation": {
                  "data": {
                    "id": "/storage/emulated/0/launcher/local/animation/あリがとゥ.gif",
                    "name": "あリがとゥ.gif",
                    "path": "/storage/emulated/0/launcher/local/animation/あリがとゥ.gif"
                  },
                  "switch": false
                },
                "ylAnimation": {
                  "data": {
                    "id": "/storage/emulated/0/launcher/local/animation/65.gif",
                    "name": "65.gif",
                    "path": "/storage/emulated/0/launcher/local/animation/65.gif"
                  },
                  "switch": false
                }
              },
              "basic": {
                "adminPass": "9999",
                "boor": "63c64050f0e02ee8af9df666",
                "char": "658260925b69eb2d91ba8b94",
                "currenttab": 0,
                "door": "65a4dd533c3781e9f18defb2",
                "fontSize": 0,
                "language": 1,
                "model": [
                  0,
                  1,
                  2,
                  3,
                  4,
                  5,
                  6
                ],
                "runMode": 3,
                "standby": "663c7977be378bb5ee8b43a2",
                "welcomeId": "65a4dd533c3781e9f18defb2",
                "welcomeModel": false,
                "welcomePlayId": 1
              },
              "cruise": {
                "countdownSwitch": true,
                "speed": 73,
                "standbyTime": 101
              },
              "delivery": {
                "countdownSwitch": true,
                "errorTraywarn": true,
                "isLineCall": true,
                "isReturn": true,
                "moderate": 0,
                "moderateSwitch": false,
                "openSmartswitch": true,
                "pallet": [
                  19,
                  ...
                ],
                "pauseDuration": 60,
                "runSpeed": 113,
                "smartList": [
                  2,
                  3
                ],
                "stopDuration": 60,
                "takeawayCountdown": 5
              },
              "footprint": [
                [
                  0.248,
                  0.108
                ],
                ...
              ],
              "forceBattery": 10,
              "lightStrip": {
                "arriveState": {
                  "lightColor": 5,
                  "lightType": 3
                },
                "chargingState": {
                  "lightColor": 3,
                  "lightType": 4
                },
                "errorState": {
                  "lightColor": 1,
                  "lightType": 2
                },
                "idleState": {
                  "lightColor": 4,
                  "lightType": 4
                },
                "lightStripSwitch": true,
                "taskState": {
                  "lightColor": 4,
                  "lightType": 1
                }
              },
              "lowBattery": 15,
              "otherSetting": {
                "footprint": [
                  [
                    0.248,
                    0.108
                  ],
                  ...
                ],
                "forceBattery": 10,
                "lightStrip": {
                  "arriveState": {
                    "lightColor": 5,
                    "lightType": 3
                  },
                  "chargingState": {
                    "lightColor": 3,
                    "lightType": 4
                  },
                  "errorState": {
                    "lightColor": 1,
                    "lightType": 2
                  },
                  "idleState": {
                    "lightColor": 4,
                    "lightType": 4
                  },
                  "lightStripSwitch": true,
                  "taskState": {
                    "lightColor": 4,
                    "lightType": 1
                  }
                },
                "lowBattery": 15,
                "skipPtDelay": 1800
              },
              "runMode": 3,
              "skipPtDelay": 1800,
              "sound": {
                "avoidVolume": 50,
                "musicFile": "/storage/emulated/0/launcher/resource/local/阿D - 1小步舞曲.mp3",
                "musicFileName": "阿D - 1小步舞曲.mp3",
                "musicVolume": 50,
                "switchon": true,
                "systemVolume": 50,
                "voiceVolume": 50
              }
            },
            "createTime": 1717053578920,
            "updateTime": 1717053578920
          }
          ...
          ```