# 保存机器人设置

## `saveRobotSetting(setting: any) -> {Promise.<boolean>}`

保存机器人设置


### 请求参数 `setting` 对象

settings
| 设置项      |         字段         |        类型      | 说明                     |
| ---------- | -------------------- | ---------------- | ------------------------ |
| settings   |          设置        |   settingsData  |     如下（settingsData）：           |

settingsData 是一个JSON对象，没有严格验证设置对象的格式，但是下面几个设置需要符合以下格式：
| 设置项      |         字段         | 类型      | 说明                     |
| ---------- | -------------------- | --------- | ------------------------ |
| 速度        | delivery.runSpeed    | number    | 速度，单位：mm/s         |
| 行驶模式    | runMode              | number    | 1：灵活避障行驶; 2： 沿轨道行驶;3： 严格沿轨道行驶 |
| 默认返航点  | basic.standby        | string    |                               |
| 默认充电桩  | basic.char           | string    |                          |
| 音量        | sound.avoidVolume    | number    | 0-10（0% - 100%）        |
| 楼层定位    | pad.foolorId         | string    |                          |
| 跳点时长    |skipPtDelay           | number    | 跳点时长，单位：s            |


### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 提示

提交机器人设置时先获取机器人设置，然后修改自己需要修改的设置内容，其它设置数据保留，然后再提交。

### 示例

```typescript
...
const settings = {
	"settings": {
		"_id": "668b47444242e2e435ba9020",
		"animation": {
			"fhAnimation": {
				"switch": false
			},
			"scAnimation": {
				"switch": false
			},
			"sleepAnimation": {
				"switch": 113
			},
			"xyAnimation": {
				"switch": false
			},
			"ylAnimation": {
				"switch": false
			}
		},
		"basic": {
			"adminPass": "9999",
			"char": "6643352e7fe5260984536181",
			"currenttab": 0,
			"door": "6643352ea3f5a3ca0463968f",
			"fontSize": 0,
			"fullCharBackRange": [],
			"language": 1,
			"model": [0, 1, 2, 3, 4, 5],
			"runMode": 2,
			"standby": "666fdf9ee85100f753742ddc",
			"welcomeId": "6673af301a0a606b23e96508",
			"welcomeModel": false,
			"welcomePlayId": 1
		},
		"buildingId": "60a4c374059acc6c8bdff074",
		"businessId": "66432c72db3008878c5dd83c",
		"carId": "2582311102392CA",
		"createTime": 1720403780458,
		"cruise": {
			"countdownSwitch": false,
			"speed": 55,
			"standbyTime": 2
		},
		"delivery": {
			"countdownSwitch": false,
			"errorTraywarn": false,
			"isLimitRotationSpeed": 0,
			"isLineCall": false,
			"isReturn": true,
			"isShelfTracking": false,
			"moderate": 0.5,
			"moderateSwitch": true,
			"openSmartswitch": true,
			"pallet": [19, 19, 19, 19],
			"pauseDuration": 26,
			"runSpeed": 67,
			"smartList": [0, 1, 2, 3],
			"stopDuration": 15
		},
		"disinfectMode": 1,
		"followSetting": {
			"max_angular_acc": 1.5,
			"max_angular_velocity": 1.5,
			"max_forward_acc": 0.6,
			"max_forward_velocity": 0.6
		},
		"footprint": [
			[-0.301, -0.344],
			[-0.301, 0.345],
			[-0.289, 0.392],
			[-0.268, 0.422],
			[-0.238, 0.442],
			[-0.132, 0.49],
			[0.132, 0.49],
			[0.238, 0.442],
			[0.268, 0.422],
			[0.289, 0.392],
			[0.301, 0.345],
			[0.301, -0.344],
			[0.296, -0.38],
			[0.274, -0.419],
			[0.244, -0.456],
			[-0.244, -0.456],
			[-0.274, -0.419],
			[-0.296, -0.38],
			[-0.301, -0.344]
		],
		"forceBattery": 10,
		"gearMode": 2,
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
				[-0.301, -0.344],
				[-0.301, 0.345],
				[-0.289, 0.392],
				[-0.268, 0.422],
				[-0.238, 0.442],
				[-0.132, 0.49],
				[0.132, 0.49],
				[0.238, 0.442],
				[0.268, 0.422],
				[0.289, 0.392],
				[0.301, 0.345],
				[0.301, -0.344],
				[0.296, -0.38],
				[0.274, -0.419],
				[0.244, -0.456],
				[-0.244, -0.456],
				[-0.274, -0.419],
				[-0.296, -0.38],
				[-0.301, -0.344]
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
		"playLanguage": 1,
		"routeMode": 1,
		"runMode": 2,
		"skipPtDelay": 1800,
		"skipPtMode": 1,
		"sound": {
			"avoidVolume": 20,
			"musicFile": "3111502",
			"musicFileName": "Minuet",
			"musicVolume": 10,
			"switchon": true,
			"systemVolume": 20,
			"voiceVolume": 20
		},
		"speedMode": 2,
		"sprayMode": 1,
		"taskId": "07005148-f47b-4abd-a63f-e42ab0be657b",
		"updateTime": 1721011302537,
		"voiceMode": 5,
		"voicePercent": 60
	}

}
const saveResult = await axRobot.saveRobotSetting(setting);
console.log(saveResult); // 操作结果
...
```

