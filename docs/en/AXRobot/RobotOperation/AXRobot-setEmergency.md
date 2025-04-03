# Set Emergency Stop

## `setEmergency(type) -> {void}`

Set the robot to enter the emergency stop state
### Parameters

| Name | Data Type | Description |
| ------ | --------------------------------------- | -------- |
| `type` | [EmergencyType](../../../Define/Define-EmergencyType) | Emergency stop method |

### Return Value

none

### Example

```javascript
...
axRobot.setEmergency(EmergencyType.Start); // enter emergency stop state
...
axRobot.setEmergency(EmergencyType.Stop); // end the emergency stop state
...
```
