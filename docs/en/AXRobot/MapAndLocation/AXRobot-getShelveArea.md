# Get Shelves Areas

## `getShelvesAreaList(req) -> {Promise.<any>}`

getShelvesAreaList

### parameters

| name  | type          | describe      | need     |
| ----- | ----------------- | ---------| -------- |
| `robotId` | string | robot Id | need |
| `isRelatedShelves` | boolean | get shelvesArea | need: true |
| `isAll` | string | get all | need: true |

### Response `Promise.<any>`

ShelvesAreaList

### Example

```typescript
...
const result = await getShelvesAreaList({robotId: 'robotId', isRelatedShelves: true, isAll: true})

const shelvesAreaList = console.log(result.list); // ShelvesAreaList
shelvesAreaList.forEach(shelvesArea => {
    //  {
        // "id": "676ba40b067a35e9f266df8c", // shelves area id
        // "name": "11", // shelves area name
        // "floor": 2, // floor
        // "floorName": "2", // floor name
        // "areaId": "676ba400295e7e9bbe03b38a", // map id
        // "coordinates": [ // shelves area coordinates - one
        // ],
        // "poiList": [ // bind shelves pois
        // ]
    // }
});
...
```

