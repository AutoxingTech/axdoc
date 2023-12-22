# ActionData - CloseDoor

Action parameters for closing the door

## Attributes

| Name | Data Type | Description |
| --------- | -------- | ---------------------------------------------- |
| `mode` | number | execution mode;<br/>1 - host computer execution<br/>2 - chassis execution |
| `doorIds` | number[] | Door number; the order is 1,2,3,4 from top to bottom and left to right |

## Example

```javascript
{
   "type": ActionType.CloseDoor,
   "data": {
     "mode": 1,
     "doorIds": [1]
   }
}
```
