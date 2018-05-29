#msgPage
```
H5:"msgPage.js"
nativeCls: "msgPage"
```

##接口变化：
```
messageApi → msgPage
	改名： 
		setMessageReaded → setMsgReaded
```

##详细接口：

###<font color='red'>setMsgReaded</font>

####简要说明：
- requireVersion：2.3.0
- 描述：通知客户端push列表消息已读



####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|messageType |是  |string |  在URD参数里面获取push消息类型 |


####callBack：无

####调用接口示例：

```
msgPage.setMsgReaded(messageType);
```
***