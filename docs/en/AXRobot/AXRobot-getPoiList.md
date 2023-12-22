# Get All Sites

## `getPoiList(req) -> {Promise.<any>}`

Get site list

### Parameters

| Name | Data Type | Description |
| ----- | ------------------------------------- | -------- |
| `req` | ​​[RequestParam](../../Define/Define-RequestParam) | Request parameters |

### Return value `Promise.<any>`

site list

### Example

```javascript
...
const result = await getPoiList({
  robotId: "<robotId>"
});

console.log(result.count); // total number of eligible POIs
console.log(result.list); // site list
result.list.forEach(poi => {
  console.log(poi.areaId); // ID of the area where the site is located
  console.log(poi.buildingId); // ID of the building where the site is located
  console.log(poi.businessId); // ID of the business to which the site belongs
  console.log(poi.floor); // The floor where the site is located
  console.log(poi.id); // site ID
  console.log(poi.name); // site name
  console.log(poi.type); // site type
  console.log(poi.coordinates); // station coordinates in the format [x, y]; eg [13.411045089526397,-6.95027412476179]
  console.log(poi.yaw); // The angle value of the site's orientation Unit: degrees
});
...
```
