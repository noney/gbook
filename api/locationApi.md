#locationApi
```
H5:"locationApi.js"
nativeCls:"locationApi"
```

##接口变化：
```
改名：
	- getLoc迁移到locationApi，改名为getCity(2.7.5)
```

##详细接口：

###<font color="red">getCity</font>

####简要描述：
- requireVersion：2.7.5
- 描述：获取地理位置

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
locationApi. getCity(function(data){
	data.citydomain //城市简写
	data.city //城市名称
	data.cityid //城市ID
}
```
***



###<font color="red">requestLocation</font>

####简要描述：
- requireVersion：2.7.5
- 描述：获取当前位置的经纬度

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
locationApi. requestLocation(function(data){
		//data.lon经度  
         //data.lat纬度
         //{lon: "116.3060115901335", lat: "40.04798410511159"}
}
```
***



###<font color="red">regeo</font>

####简要描述：
- requireVersion：2.7.5
- 描述：根据经纬度获取地理位置

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
locationApi. regeo(function(data){
		//POI信息 {address: "北京市海淀区东北旺路"}
}
```
***




###<font color="red">geo</font>

####简要描述：
- requireVersion：2.7.5
- 描述：根据城市街道获取经纬度

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|address |是  |string | address为结构化地址信息（规则：省+市+区+街道+门牌号）|
|city |是  |string | 城市名称例如"北京"|

####callback：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####接口调用示例：
```
locationApi. regeo(address,city,function(data){
		//{lat: "40.04972406559961", lon: "116.3023880280724"}
}
```
***


###<font color="red">requestPOI</font>

####简要描述：
- requireVersion：2.7.5
- 描述：获取当前兴趣点

####参数：

无

####callback：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####接口调用示例：
```
locationApi. regeo(address,city,function(data){
		{
                           address: "北京市海淀区东北旺路", 
                           district: "海淀区", 
                           city: "北京", 
                           streetName: "东北旺路", 
                           streetNumber: "",
                           lon: "116.3060115901335",
                          lat: "40.04798410511159",
                          province: "北京市"
             }
}
```
***




###<font color="red">searchPOIAround</font>

####简要描述：
- requireVersion：2.7.5
- 描述：获取周边商圈

####参数：

无

####callback：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####接口调用示例：
```
locationApi. regeo(address,city,function(data){
		//周边POI信息 {businessCircle: "上地,马连洼,西二旗"}
}
```



###<font color="red">getCachedLocation</font>

####简要描述：
- requireVersion：3.0.0
- 描述：获取首页缓存里面的经纬度

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
locationApi.getCachedLocation(function(data){
    //data.lon经度  
    //data.lat纬度
    //{lon: "116.3060115901335", lat: "40.04798410511159"}
}
```
***