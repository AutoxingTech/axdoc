# Get Robot Footprint

## `getRobotFootprint() -> {Promise.<any>}`

Obtain robot contour lines


### Parameters
none

### Return value `Promise.<any>`


| Name  | Data Type | Description                    |
| ------ | ------ | ------------------------ |
| `footprint` | Array | Robot contour line collection |


### Example

```typescript
...
const footprintData = await axRobot.getRobotFootprint();
console.log(footprintData.footprint); // Robot contour line collection
...
```

