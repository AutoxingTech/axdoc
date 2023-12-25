# Cabin Door Control

## Methods

## `openBoxDoor(doorIds, mode) → {Promise.<boolean>}`

Open the box door

### Parameters

| Name | Type | Required | Description |
| --------- | -------- | ---- | ----------------------------------------- |
| `doorIds` | number[] | Yes | A list of door numbers, ranging from 1 to 4. |
| `mode` | number | no | Execution mode: 1=host computer, 2=chassis; default: 1. |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
// Open the door of box 1
const success = await axRobot.openBoxDoor([1], 1);
...
```



## `closeBoxDoor(doorIds, mode) → {Promise.<boolean>}`

close the door

### Parameters

| Name | Type | Required | Description |
| --------- | -------- | ---- | ----------------------------------------- |
| `doorIds` | number[] | Yes | A list of door numbers, ranging from 1 to 4. |
| `mode` | number | no | Execution mode: 1=host computer, 2=chassis; default: 1. |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
// close door 2
const success = await axRobot.closeBoxDoor([2], 1);
...
```
