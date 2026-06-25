````markdown
# Get All POI Sites

## `getPoiListExtend(req) -> {Promise.<any>}`

Get POI site list. Previously, getting sites required specifying a robot. If no robot was specified, it would default to querying site data for the connected robot. Now it has been extended to allow querying corresponding site data by combining business, area, and robot in any combination.

### Parameters

| Name  | Data Type                              | Description     |
| ----- | ------------------------------------- | -------- |
| `req` | [RequestParam](../../Define/Define-RequestParam.md) | Request parameters |

### Return Value `Promise.<any>`

Site list

### Example

```typescript
...
const result = await getPoiListExtend({
  businessId: "<businessId>", // Optional (one of)
  areaId: "<areaId>", // Optional (one of)
  robotId: "<robotId>" // Optional (one of)
});

console.log(result.count); // Total number of POIs matching the criteria
console.log(result.list); // Site list
result.list.forEach(poi => {
  console.log(poi.areaId); // Area identifier where the site is located
  console.log(poi.buildingId); // Building identifier where the site is located
  console.log(poi.businessId); // Business identifier the site belongs to
  console.log(poi.floor); // Floor where the site is located
  console.log(poi.id); // Site identifier
  console.log(poi.name); // Site name
  console.log(poi.type); // Site type
  console.log(poi.coordinates); // Site coordinates, format: [x, y]; e.g., [13.411045089526397,-6.95027412476179]
  console.log(poi.yaw); // Site orientation angle, unit: degrees
});
...
```


````
