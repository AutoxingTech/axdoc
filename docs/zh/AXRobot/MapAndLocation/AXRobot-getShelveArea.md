# 获取货架区

## `getShelvesAreaList(req) -> {Promise.<any>}`

获取货架区列表

### 参数

| 名称  | 数据类型          | 说明      | 必须     |
| ----- | ----------------- | ---------| -------- |
| `robotId` | string | 机器人id | 必须 |
| `isRelatedShelves` | boolean | 获取货架区 | 必须：true |
| `isAll` | string | 获取所有货架区域 | 必须：true |

### 返回值 `Promise.<any>`

站点列表货架区列表

### 示例

```typescript
...
const result = await getShelvesAreaList({robotId: 'robotId', isRelatedShelves: true, isAll: true})

const shelvesAreaList = console.log(result.list); // 货架区列表
shelvesAreaList.forEach(shelvesArea => {
    //  {
        // "id": "676ba40b067a35e9f266df8c", // 货架区id
        // "name": "11", // 货架区名称
        // "floor": 2, // 楼层
        // "floorName": "2", // 楼层名称
        // "areaId": "676ba400295e7e9bbe03b38a", // 货架地图id
        // "coordinates": [ // 货架区坐标点
        // ],
        // "poiList": [ // 货架区内绑定的货架POI列表
        // ]
    // }
});
...
```

