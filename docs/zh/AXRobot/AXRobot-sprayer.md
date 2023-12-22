# 喷雾器控制

## 方法

## `openSprayer(gear) → {Promise.<boolean>}`

打开喷雾器

### 参数

| 名称   | 类型   | 说明 |
| ------ | ------ | ---- |
| `gear` | number | 档位 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.openSprayer("<gear>");
...
```



## `closeSprayer() → {Promise.<boolean>}`

关闭喷雾器
### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.closeSprayer();
...
```