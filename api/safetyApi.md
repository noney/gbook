#safetyApi
```
H5:"safetyApi.js"
nativeCls:"safetyApi"
```

##接口变化：
```
迁移：
	- dekEncrypt，dekDecrypt  clientInfo→safetyApi(2.7.5)
```
###<font color="red">dekEncrypt</font>

####简要描述
- requireVersion：2.4.0
- 描述：dek加密

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| info |是  |string | 需要加密的字段|
| callBack |是  |function | 客户端执行的回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |string | 加密之后返回的字符串|

####调用接口示例：
```
safetyApi. dekEncrypt(function(info){
    console.log(info);
});
```
***
###<font color="red">dekDecrypt</font>

####简要描述
- requireVersion：2.4.0
- 描述：dek解密



####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| info |是  |string | 需要解密的字段|
| callBack |是  |function | 客户端执行的回调函数|

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |string | 解密之后返回的字符串|

####调用接口示例：
```
safetyApi. dekDecrypt(function(info){
    console.log(info);
});
```
***
