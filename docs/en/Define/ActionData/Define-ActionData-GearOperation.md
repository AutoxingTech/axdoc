# ActionData - GearOperation

Operation parameters of sprayer

## Attributes

| Name | Data Type | Description |
| --------- | -------- | -------------------------------------------------- |
| `subType` | number | Spray action parameters; <br/>0: close spray, 1-5 set gear, open spray |

## Example

```javascript
{
   "type": ActionType.GearOperation,
   "data": {
     "subType": 2
   }
}
```
