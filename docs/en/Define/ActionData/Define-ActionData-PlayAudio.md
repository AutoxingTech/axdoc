# ActionData - PlayAudio

Play Audio Action Parameters

## Attributes

| Name | Data Type | Description |
| ---------- | -------- | ------------------------------------------------------------ |
| `audioId` | string | optional;<br/>local audio resource identifier, default is filename |
| `url` | string | optional; <br/>audio online URL |
| `volume` | number | volume; 0~100 |
| `mode` | number | execution mode;<br/>1 - host computer execution<br/>2 - chassis execution |
| `interval` | number | Interval time for loop playback; unit: seconds<br/>-1 means play only once |
| `num` | number | optional; number of plays |
| `duration` | number | optional; total playback time; unit: seconds<br/>If the `num` parameter is also set, the `num` parameter setting shall prevail |
| `channel` | number | playback channel;<br/>1 - normal music<br/>2 - background music<br/>The chassis does not support multi-channel playback |

## Example

```javascript
{
  "type": ActionType.PlayAudio,
  "data": {
    "audioId": "3111001",
    "volume": 50,
    "mode": 1,
    "interval": 20,
    "num": 10,
    "channel": 1
  }
}
```
