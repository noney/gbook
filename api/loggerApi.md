#loggerApi

```
H5:"loggerApi.js"
nativeCls:"loggerApi"
```

##接口变化：

```
移动

	- addLog （clientInfo→loggerApi）（2.7.5）
```

###<font color="red">addLog</font>
####简要描述：
- requireVersion：2.7.5
- 描述：收集统计

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| type |是  |string | 日志类型  0 talkingData统计 1 斗米平台pv统计 2 斗米平台ev统计 6 针对于dmuch与该页面pv不一致的情况下|
| log |是  |string | 日志内容|
| pv  |是  |string | 该页面pv信息(type为6时传该参数)|
| ev  |是  |string | ev信息(type为6时传该参数)|

####callback：无

####调用接口示例：
```
loggerApi.addLog(type,log);
loggerApi.addLog(6,'',pv,ev);
```
***
###<font color="red">addTDAdTrackingLog</font>
####简要描述：
- requireVersion：3.7.1
- 描述：收集广告统计

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| type |是  |string | 广告类型  1-10|

####callback：无

####调用接口示例：
```
loggerApi.addTDAdTrackingLog('10');
```
***