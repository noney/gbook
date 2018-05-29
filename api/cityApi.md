#cityApi
```
H5:"cityApi.js"
nativeCls:"cityApi"
```

##接口变化：
```
改名：
	- getPosition → getLoc
	- getUserSelectCity → getValidCity
迁移：
	- getLoc迁移到locationApi，改名为getCity(2.7.5)
	- showCityPicker  clientUI→cityApi(2.7.5)
```

##详细接口：

###<font color="red">getValidCity</font>
####简要描述：
- requireVersion：2.6.0
- 描述：获取用户选择城市

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callback |是  |function | 回调函数|

####callback：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####接口调用示例：
```
cityApi.getValidCity(function(data){
	data.cityid //城市ID
	data.citydomain //城市名称首字母
}
```
***

###<font color="red">changeCity</font>

####简要描述：

- requireVersion：2.1.0
- 描述：切换城市

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| jsonParam |是  |object | 切换城市所需要的参数domain,cityname,cityid|

####callBack：无

####调用接口示例：

```
cityApi.changeCity(jsonParam)；
```
***

###<font color="red">showCityPicker</font>

####简要说明：
- requireVersion：2.4.0
- 描述：H5调起地址筛选框

####参数:
无

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
cityApi. showCityPicker(function(data){
	// {"status":1,"cityId":12,"cityName":"北京","selected":[{"name":"昌平","id":185},{"name":"立水桥","id":185}]}  街道可能会不存在
});
```	
***