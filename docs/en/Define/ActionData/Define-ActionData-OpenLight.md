# ActionData - OpenLight

Turn on the light strip action parameter Action parameter

## Attributes

| Name | Data Type | Description |
| -------- | --------------------------------- | ---------------------------------------------- |
| `mode` | number | execution mode;<br/>1 - host computer execution<br/>2 - chassis execution |
| `color` | [LightColor](../../Define-LightColor) | Strip color |
| `indexs` | [LightIndex](../../Define-LightIndex) | Optional; segment display, currently supports up to 4 segments |

## Example

```javascript
{
   "type": ActionType.OpenLight,
   "data": {
     "mode": 1,
     "color": LightColor.Green,
     "indexes": [
       {
         "index": 0,
         "num": 10
       }
     ]
   }
}
```
