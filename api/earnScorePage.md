#earnScorePage
```
H5:"earnScorePage"
nativeCls:"earnScorePage"
```

##接口变化：
```
2.8.0 新增，积分数据结构统一由客户端管理
```

##详细接口：

###<font color="red">getData</font>

####简要描述：
- requireVersion：2.8.0
- 描述：向客户端获取积分数据

####参数:
无
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：
```
earnScorePage.getData(function(data){ //1 完成 0 未完成 
	{ //data 
		signin:1, //1 已签到 0 未签到
		sharetegong:1, //分享特工
		posts:1, //浏览帖子
		resume:1, //简历
		IDCard:1, //认证
		preference:1, //偏好
		apply:1, //申请
		duiba:1 //商城
	}
});
```
***


###<font color="red">pullData</font>

####简要描述：
- requireVersion：2.8.0
- 描述：通知客户端需要跟新积分数据

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|pullData |是  |number | 1需要更新 0 不需要  |
####callBack：
无

####调用接口示例：
```
earnScorePage.pullData(1);
```
***

###<font color="red">signIn</font>

####简要描述：
- requireVersion：2.8.0
- 描述：调用客户端签到接口，签到成功跳成功页面，失败客户端弹toast

####参数:
无
####callBack：
无

####调用接口示例：
```
earnScorePage.signIn();
```
***