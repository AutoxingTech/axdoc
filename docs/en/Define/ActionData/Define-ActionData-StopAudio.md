# ActionData - StopAudio

stop playing audio action parameter

## Attributes

| Name | Data Type | Description |
| --------- | -------- | ------------------------------------------------------------ |
| `mode` | number | execution mode;<br/>1 - host computer execution<br/>2 - chassis execution |
| `channel` | number | playback channel;<br/>1 - normal music<br/>2 - background music<br/>The chassis does not support multi-channel playback |

## Example

```javascript
{
   "type": ActionType.StopAudio,
   "data": {
     "mode": 1,
     "channel": 1
   }
}
```

###
