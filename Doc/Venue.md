Venue
---
>By zjien

##**管理员**
##### 以下接口只适用于管理员

#### **创建场馆**
`/Admin/Manager/createVenue` `POST`

字段 | 描述 | 是否必须 | 数据类型 | 备注
------------------------- | -------------------------- | :-----------------------: | --------------------------- | ----------------------
name | 场馆名字 | Y | string | 
people | 能提供的预定数 | Y | int |
picture | 场馆的图片 | N | string | 默认是一张空图片
type | 能提供运动项目 | N | string |
price | 价格 | Y |  int |/每小时
region | 所在城市 | N | string | 
intro | 简介 | N | string | 

#####返回字段解释：
字段 | 描述 | 是否必须 | 数据类型 | 备注
------------------------- | -------------------------- | :-----------------------: | --------------------------- | ----------------------
va_id | 场馆id |  | int | 
ma_id | 管理员id |  | int |
booked | 目前预订人数 |  | int |
bought | 预订历史数 |  | int |
last_time | 最后一次更新时间 |  | int
last_IP | 最后一次更新IP |  | int 
**Response**  
```json
{
    "code": 20000,
    "response": {
        "vi_id": "1",
        "ma_id": "3",
        "name": "myVenue",
        "people": "5",
        "booked": "0",
        "picture": "a default pic",
        "type": "羽毛球,足球",
        "price": "25",
        "bought": "0",
        "region": "江门",
        "intro": null,
        "last_time": "1422430617",
        "last_IP": "127.0.0.1"
    }
}
```
---

#### **更新场馆**
`/Admin/Manager/updateVenue` `POST`

字段 | 描述 | 是否必须 | 数据类型 | 备注
------------------------- | -------------------------- | :-----------------------: | --------------------------- | ----------------------
vi_id | 场馆id | Y | int | 
people | 能提供的预定数 | N | int |
picture | 场馆的图片 | N | string | 默认是一张空图片
type | 能提供运动项目 | N | string |
price | 价格 | N |  int |/每小时
intro | 简介 | N | string | 
**Response**  
```json
{
    "code": 20000,
    "response": {
        "vi_id": "1",
        "ma_id": "3",
        "name": "myVenue",
        "people": "5",
        "booked": "0",
        "picture": "a new pic",
        "type": "羽毛球,足球",
        "price": "25",
        "bought": "0",
        "region": "江门",
        "intro": null,
        "last_time": "1422430617",
        "last_IP": "127.0.0.1"
    }
}
```
---

#### **场馆暂停营业**
`/Admin/Manager/closeVenue` `POST`

字段 | 描述 | 是否必须 | 数据类型 | 备注
------------------------- | -------------------------- | :-----------------------: | --------------------------- | ----------------------
vi_id | 场馆id | Y | int | 
**Response**
```json
{
    "code": 20000,
    "response": "操作成功"
}
```
---

#### **场馆开放营业**
`/Admin/Manager/openVenue` `POST`

字段 | 描述 | 是否必须 | 数据类型 | 备注
------------------------- | -------------------------- | :-----------------------: | --------------------------- | ----------------------
vi_id | 场馆id | Y | int | 
**Response**
```json
{
    "code": 20000,
    "response": "操作成功"
}
```
---