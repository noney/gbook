#ol_indexPage
```
H5:"ol_indexPage"
nativeCls:"ol_indexPage"
```

##接口变化：
```
ol_indexApi → ol_indexPage
```

##详细接口：

###<font color="red">setFilterMenu</font>

####简要描述：
- requireVersion：2.6.0
- 描述：设置FilterMenu距离顶部的高度,Menu的高度,Menu的数据


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|height |是  |number | 设置filterMenu 的高度  |
|opacityHeight |是  |number | 设置Menu的高度  |
|menuData |是  |object | 设置Menu的数据，把服务端返回的Menu数据提供给客户端  |
####callBack：无

####调用接口示例：
```
ol_indexPage.setFilterMenuOffset(height, opacityHeight,menuData)
```
***

###<font color="red">clickFilterMenu</font>

####简要描述：
- requireVersion：2.6.0
- 描述：通知客户端用户点击H5FilterMenu


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|index |是  |number | 通知客户端点击menu的位置  |
####callBack：无

####调用接口示例：
```
ol_indexPage.clickFilterMenu(index)
```
***


###<font color="red">readOlStartupState</font>

####简要描述：
- requireVersion：2.6.5
- 描述：判断客户端是否是首次启动


####参数:
无
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####调用接口示例：
```
ol_indexPage. readOlStartupState(function(data){
	data.state==1 //首次启动  0 非首次
});
```
***

