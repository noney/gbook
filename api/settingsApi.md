#settingsApi
```
H5:"settingsApi"
nativeCls:"settingsApi"
```

##接口变化：
```
➕settingsApi
```

##详细接口：

###<font color="red">setIMNotifyStatus</font>

####简要描述：
- requireVersion：2.4.0
- 描述：设置IM消息通知的开关

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|status |是  |number | 需要设置的状态 0 关闭 1 开启 |
|callBack |是  |function | 回调函数|


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```     settingsApi.setIMNotifyStatus(status,function(data){
	data.status//0 设置失败 1 设置成功
})
```
***

###<font color="red">getIMNotifyStatus</font>

####简要描述：
- requireVersion：2.4.0
- 描述：获取IM消息通知的开关

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callBack |是  |function | 回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
settingsApi.getIMNotifyStatus(function(data){
	data.status //0 关闭 1 开启
})
```
***