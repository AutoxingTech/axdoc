# TaskPoint

task node information

## Attributes

| Name | Data Type | Description |
| ---------- | ----------------------------------- | ---------------------------- |
| `areaId` | string | The ID of the map area where the task node is located |
| `x` | number | task node coordinate x component |
| `y` | number | task node coordinate y component |
| `yaw` | number | The orientation of the task node; unit: angle |
| `type` | number | POI type; Reference: [POI Types](../../Define/Define-PoiType) |
| `ext` | object | optional; task node custom extension information |
| `stepActs` | [BaseAction](../../Define/Define-BaseAction)[] | optional; task node action list |

## Example

```json
{
  "x": 0.11,
  "y": 1.22,
  "yaw": 89,
  "areaId": "xxxx",
  "type": -1,
  "ext": {...},
  "stepActs": [...]
}
```
