#deviceApi
```
H5:"deviceApi"
nativeCls:"deviceApi"
```

##接口变化：
```
	增加：
		- 2.9.0新增 
```

##详细接口：

###<font color="red">openGPSSetting</font>

####简要描述：
- requireVersion：2.9.0
- 描述：调起客户端定位设置页面，从设置返回客户端调用H5的window.refreshNearbyJobPage

####参数:
无

####callBack：
无

####调用接口示例：	

```
	KCdeviceApi.openGPSSetting()
```
***


###<font color="red">copyToClipboard</font>

####简要描述：
- requireVersion：2.9.0
- 描述：复制到剪贴板

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|content |是  |string | 需要复制到剪贴板的内容  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	

```
	KCdeviceApi.copyToClipboard(info, function(data){
		data.status // 0 复制失败 1 复制成功
	});
```
***