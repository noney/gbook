#searchPage

##详细接口：

###<font color="red">searchKey</font>

####简要描述：
- requireVersion：2.6.5
- 描述：客户端通知H5用户输入的关键字


####参数:
无
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####调用接口示例：
```
searchPage.searchKey(function(data){
	data. searchKey
});
```
***

###<font color="red">setFilterMenu</font>

####简要描述：
- requireVersion：3.6.0
- 描述：设置筛选框是否显示


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|isShow |是  |boolean | 设置筛选框是否显示  |
####callBack：无

####调用接口示例：
```
searchPage.setFilterMenu(true)
```
***