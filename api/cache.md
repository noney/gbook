#cache
<font style="color:blue;">H5和客户端参数字段保持一致</font>

```
H5:"cache"
nativeCls:"cache"
```

##接口变化：

```
	增加：
		- setCache （clientInfo→cache）
		- getCache  （clientInfo→cache）
		- deleteCache
		- clearCache  （默认清除所有Cache）（待定）
		- clearMemoryCache  （默认清除所有MemoryCache）（待定）
		- clearAllCache（待定）
```
##详细接口：

###<font color='red'>setCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：设置本地缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 设置本地缓存的键值，需要依据键值去取缓存|
| cacheData |是  |object | 设置本地缓存的值，取出来需要渲染的数据|
| cacheTime |是  |number | 缓存时间|

####callBack：无

####调用接口示例：
```
cache.setCache(cacheKey, cacheData,cacheTime);
```
***

###<font color='red'>getCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：获取本地缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 获取本地缓存的键值|
| cacheData |是  |function | 客户端执行的回调函数|

####callBack：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数时的返回值，setCache里面存贮的值，如果对应的cacheKey没有值，则返回null|

####调用接口示例：
```
cache.getCache(cacheKey,callBack);
```
***

###<font color='red'>deleteCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：删除本地缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 删除本地缓存的键值|

####callBack：无

####调用接口示例：
```
cache.deleteCache(cacheKey);
```
***

###<font color='red'>setMemoryCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：设置内存缓存，杀掉APP自动清除

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 设置内存缓存的键值，需要依据键值去取缓存|
| cacheData |是  |object | 设置内存缓存的值，取出来需要渲染的数据|

####callBack：无

####调用接口示例：
```
cache. setMemoryCache(cacheKey, cacheData);
```
***

###<font color='red'>getMemoryCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：获取内存缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 获取内存缓存的键值|
| cacheData |是  |function | 客户端执行的回调函数|

####callBack：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调函数时的返回值，setMemoryCache里面存贮的值，如果对应的cacheKey没有值，则返回null|

####调用接口示例：
```
cache.getMemoryCache(cacheKey,callBack);
```
***

###<font color='red'>deleteMemoryCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：删除内存缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| cacheKey |是  |string | 删除内存缓存的键值|

####callBack：无

####调用接口示例：
```
cache.deleteMemoryCache(cacheKey);
```
***


###<font color='red'>clearCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：清除本地缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| type |是  |number | 需要清除的缓存类型  默认全部清除type为0，type为1 清除H5的缓存|

####callBack：无

####调用接口示例：
```
cache.clearCache(type);
```
***

###<font color='red'>clearMemoryCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：清除内存缓存

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| type |是  |number | 需要清除的缓存类型  默认全部清除type为0，type为1 清除H5的缓存|

####callBack：无

####调用接口示例：
```
cache.clearMemoryCache(type);
```
***

###<font color='red'>clearAllCache</font>
####简要描述：
- requireVersion：2.6.0
- 描述：清除所有缓存，本地和内存，不区分native和H5

####参数：无

####callBack：无

####调用接口示例：
```
cache.clearAllCache();
```
***