# 设置/更新巡游路线

## `saveCruise(cruiseInfo) -> {Promise<boolean>}`

设置/更新巡游路线

### 参数

| 名称         | 类型                              | 说明         |
| ------------ | --------------------------------- | ------------ |
| `cruiseInfo` | [CruiseInfo](../../Define/Define-CruiseInfo) | 巡游路线信息 |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 示例

```typescript
...
let cruiseInfo = {
    id: 12,
    name: "test-cruise",
    businessId: "",
    sites: [{
        poiId: "6423afdb1162805312f27a75",
        poiName: "test-poi"
    }],
    remark: ""
}
const success = await axRobot.saveCruise(cruiseInfo);
...
```
