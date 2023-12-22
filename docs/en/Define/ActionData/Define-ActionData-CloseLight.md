# ActionData - CloseLight

Turn off the light strip action parameter

## Attributes

| Name | Data Type | Description |
| -------- | --------------------------------- | ---------------------------------------------- |
| `mode` | number | execution mode;<br/>1 - host computer execution<br/>2 - chassis execution |
| `indexs` | [LightIndex](#/Define-LightIndex) | Optional; segment display, currently supports up to 4 segments |

## Example

```javascript
{
   "type": ActionType.OpenLight,
   "data": {
     "mode": 1,
     "indexes": [
       {
         "index": 0,
         "num": 10
       }
     ]
   }
}
```
