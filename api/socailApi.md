#socailApi
```
H5:"socailApi"
nativeCls:"socailApi"
```

##接口变化：
```
	增加：
		- 调起支付宝支付功能（待定） 
		- share（widget→socialApi） 
```

##详细接口：

###<font color="red">bindWeinxin</font>

####简要描述：
- requireVersion：2.2.0
- 描述：调用客户端接口，客户端去绑定微信，并返回微信信息

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	

```
	socialApi.bindWeixin(function(data){
		console.log(data); //data.nickname data.openid
	});
```
***

###<font color="red">share</font>

####简要描述：
- requireVersion：2.6.0
- 描述：分享

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|shareData |是  |json | 分享信息  |
|from |是  |string | 来源  |
|shareType |是  |number | 类型  |

####callBack: 无

####调用接口示例：
```
socialApi.share(json);
```
***

###<font color="red">shareTaoImage</font>

####简要描述：
- requireVersion：3.6.0
- 描述：分享

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|shareData |是  |json | 分享信息  |

####callBack: 无

####调用接口示例：
```
socialApi.shareTaoImage(json);
```
***

###<font color="red">shareTaoCode</font>

####简要描述：
- requireVersion：3.6.0
- 描述：分享

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|shareText |是  |string | 分享信息  |
|id |是  |number | 商品id  |

####callBack: 无

####调用接口示例：
```
socialApi.shareTaoImage(shareText, id);
```
***


###<font color="red">olInviteShare</font>

####简要描述：
- requireVersion：2.7.0
- 描述：特工分享，有客户端去服务端统一取数据

####参数:
无

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	

```
	socialApi.bindWeixin(function(data){
	
		 data.status==1 //成功  
		 data.stateType  //分享的路径   QQ,微信等  
	});
```
***