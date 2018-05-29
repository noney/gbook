#clientInfo
```
H5:"clientInfo"
nativeCls:"clientInfo"
```

##接口变化：
```
删除：
	- getRequestParam 
	- makePhoneCall 
	- getWebImageCacheDir(安卓)
移动：
	- goBack （clientInfo→page）
	- dataDownloadFinished （clientInfo→page）
	- setCache、getCache等一系列Cache （clientInfo→page）
	- addLog (clientInfo→loggerApi)(2.7.5)
	- dekEncrypt, dekDecrypt迁移到safetyApi（2.7.5）
修改：
	- addLog 增加参数type
```

##详细接口：

###<font color="red">getHost</font>

####简要描述：
- requireVersion：1.0.0
- 获取服务端的接口域名

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callBack |是  |function | 回调函数|

####callback：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| host |是  |object | 回调函数的返回值|

####调用接口示例：
```
clientInfo.getHost(function(host{    
	console.log(host.info);
}
```
***


###<font color="red">getNetworkType</font>
####简要描述：
- requireVersion：1.0.0
- 判断当前网络状态

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callback |是  |function | 回调函数|

####callBack:

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| status |是  |object | 回调函数执行时的返回值|

####调用接口示例：
	
```
clientInfo.getNetworkType(function(status){
  console.log(status.network); //网络类型
}

```
***

###<font color="red">getDeviceToken</font>

####简要描述

- requireVersion：2.3.0
- 获取deviceToken



####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callBack |是  |function | 客户端执行的回调函数|

####callBack：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数的返回值|

####调用接口示例：
```
clientInfo.getDeviceToken(function(data){
    console.log(data.deviceToken);
});
```
***
###<font color="red">getAccessToken</font>
####简要描述：
- requireVersion：2.2.0
- 获取accessToken

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callBack |是  |function | 客户端执行的回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数的返回值|

####调用接口示例：
```
clientInfo.getAccessToken(function(data){
    console.log(data.accessToken);
});
```
***

###<font color="red">getCommonHeaders</font>

####简要说明：
- requireVersion：2.2.0
- 获取公共headers

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callBack |是  |function | 客户端执行的回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数的返回值|

####调用接口示例：
```
clientInfo.getCommonHeaders(function(data){
    console.log(data);//cookie accessToken info 等
});
```
***

###<font color="red">getCookie</font>

####简要描述：
- requireVersion：2.2.0
- 获取cookie

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| callBack |是  |function | 客户端执行的回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数的返回值|

####调用接口示例：
```
clientInfo.getCookie(function(data){
    console.log(data.cookie);
});
```
***

