# Get List Of Area

## `getAreaList() -> {Promise.<any>}`

Get a list of regions

### Parameters

none

### Return value `Promise.<any>`

area list

### Example

```javascript
...
const result = await axRobot.getAreaList();

const data = result.data
console.log(data.count); // number of map areas
console.log(data.list); // map area list
data.list.forEach(area => {
   console.log(area.id); // area ID
   console.log(area.buildingId); // The building ID of the area
   console.log(area.businessId); // The business ID of the area
   console.log(area.name); // area name
   console.log(area.floor); // area is on floor
   console.log(area.createTime); // area creation time
});
...
```
