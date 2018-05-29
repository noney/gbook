#UCApi
```
H5:"UCApi"
nativeCls:"UCApi"
```

##接口变化：
```
userCenterApi 拆分成UCApi、UCPage
	删除：
		- mobileCode
		- userInfo
		- cashList
		- userBalance
		- applyCash
		- inviteCode
		- applyList
		- userStatus
	修改：
	- getUser → getUserInfo(UCApi)
	- setUserInfo  增加参数job_prefer_audit
```

##详细接口：


###<font color="red">logIn</font>

####简要说明：
- **requireVersion：** 2.3.0
- 描述：登录，H5把手机号，验证码通知给客户端，客户端去发送请求



####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|mobile |是  |string | 用户电话号码  |
|code |是  |string | 用户手机收到的验证码  |
|psw |否  |string | 用户密码  |
|json |否  |string | 预留扩展参数  |
|callBack |否  |string | 预留扩展参数  |

####callBack：无

####调用接口示例：
```
UCApi.logIn(mobile,code,psw,json,function(data){
	//返回json格式数据
});
```

####修改记录:
|修改记录|version | requireVersion|作者|时间|
|:----   |:--- |:---|:----- |-----   |
|参数修改：phoneNumber改为mobile，verifyCode改为code，更加psw,json,callBack |1.0.6|2.3.0  |李勇 | 2016.3.11  |


***

###<font color="red">register</font>

####简要说明：
- **requireVersion：** 2.4.0
- 描述：注册，H5把手机号，验证码，密码通知给客户端，客户端去发送请求

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|mobile |是  |string | 用户电话号码  |
|code |是  |string | 用户手机收到的验证码  |
|password |是  |string | 用户密码  |
|json |否  |string | 预留扩展参数  |
|callBack |否  |string | 预留扩展参数  |

####callBack：无

####调用接口示例：

```
UCApi.register(mobile,code,password,json,function(data){
	//返回json格式数据
});
```
***

###<font color="red">reset</font>

####简要说明：
- **requireVersion：** 2.4.0
- 描述：重置代码，H5把手机号，验证码，密码通知给客户端，客户端去发送请求



####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|mobile |是  |string | 用户电话号码  |
|code |是  |string | 用户手机收到的验证码  |
|password |是  |string | 用户密码  |
|json |否  |string | 预留扩展参数  |
|callBack |否  |string | 预留扩展参数  |

####callBack：无

####调用接口示例：

```
UCApi.reset(mobile,code,password,json,function(data){
	//返回json格式数据
});
```
***

###<font color="red">logOut</font>

####简要描述：
- requireVersion：1.0.0
- 描述：退出登录，通知客户端用户退出登录，客户端删除本地用户信息

####参数：无

####callBack：无

####调用接口示例：

```
UCApi.logOut();
```
***

###<font color="red">getUserInfo</font>

####简要描述：
- requireVersion：2.3.0
- 获取用户信息


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
UCApi.getUserInfo(function(data){
	console.log(data);
});
```
***

###<font color="red">setUserInfo</font>
####简要说明：
- requireVersion：2.3.0
- 描述：把用户信息交由客户端保存


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|userId |是  |string | 用户id  |
|grade |是  |string | 用户等级 |
|score |是  |string | 用户积分  |
|score_rate |是  |object | 等级基础分，倍率  |
| job_prefer_audit |是  |number | 1 已经设置职位偏好 0 没有设置  |

####callBack：无

####调用接口示例：

```
UCApi.setUserInfo(userId,grade,score,score_rate,job_prefer_audit);
```
***

###<font color="red">reloadUCPageWhenAppear</font>
####简要说明：
- requireVersion：3.7.0
- 描述：刷新个人中心页标记，调用当个人中心页出现时则刷新


####参数: 无

####callBack：无

####调用接口示例：

```
UCApi.reloadUCPageWhenAppear();
```
***

###<font color="red">changePhoneNumber</font>
####简要说明：
- requireVersion：3.8.0
- 描述：更换手机号


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|mobile |是  |string | 手机号  |
|code |是  |string | 验证码 |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：

```
UCApi.changePhoneNumber(userId,grade,score,score_rate,job_prefer_audit);
```
***