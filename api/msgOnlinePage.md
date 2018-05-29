#msgOnlinePage
```
H5:"msgOnlinePage"
nativeCls:"msgOnlinePage"
```

##接口变化：
```
    增加：
        - 3.3.0新增 
```

##详细接口：

###<font color="red">getOnlineList</font>

####简要描述：
- requireVersion：3.3.0
- 描述：获取特工通知消息数据

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|page |是  |number |  数据当前页 |
|pageSize |是  |number |  每页数据量 |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####调用接口示例： 

```
    msgOnlinePage.getInviteList(1, 5, function(data){
        data.status = 'success'/'error'/'nonet' //请求状态
        data.data //消息数据
        data.message //请求信息
    } )
```
***