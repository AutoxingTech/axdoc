# TaskStatistics

Task Statistics Info

## Attributes

| Name | Data Type | Description |
| ----------- | -------- | ----------------------------------------------------------- |
| `startTime` | number   | Start time, unit: milliseconds, starting at 00:00:00 of the current day, and the maximum time is one month |
| `endTime`   | number   | End data, unit: millisecond, end at 11:59:59 of the current day                  |
| `type`      | number   | Task type<br/>0 - Disinfect<br/>1 - Go home<br/>2 - Delivery<br/>3 - Summoning<br/>Default -1 All       |

## Example

```json
{
  "startTime": 1682870400000,
  "endTime": 1685548799000,
  "type": -1
}
```
