# getPoiListExtend

## `getPoiListExtend(req) -> {Promise.<any>}`

To obtain a list of sites, it was necessary to pass on the vehicle before obtaining the site. If the vehicle is not passed on, the data of the connected site will be queried by default. Now, it has been expanded to be able to query corresponding site data based on any combination of query conditions such as business, region, and robot.

### Parameters

| Fields       | Type | Description     |
| ----- | ------------------------------------- | -------- |
| `req` | [RequestParam](../../../Define/Define-RequestParam) | req |

### Return Value `Promise.<any>`

PoiList

### Example

```typescript
...
const result = await getPoiListExtend({
  businessId: "<businessId>", 
  areaId: "<areaId>", 
  robotId: "<robotId>" 
});

console.log(result.count); 
console.log(result.list); 
result.list.forEach(poi => {
  console.log(poi.areaId); 
  console.log(poi.buildingId); 
  console.log(poi.businessId); 
  console.log(poi.floor); 
  console.log(poi.id); 
  console.log(poi.name);
  console.log(poi.type);
  console.log(poi.coordinates); 
  console.log(poi.yaw);
});
...
```

