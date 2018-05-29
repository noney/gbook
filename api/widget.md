#widget
```
H5:"widget"
nativeCls:"widget"
```

##接口变化：
```
	移动：
		- share（widget→socialApi）
		- loadState 移到 page 改为 loadPageStatus
		- getNavbarHeight 移到 page
		- setPullToRefreshWebView 移到 page 改为 canPullWebView
```

##详细接口：

###<font color="red">toast</font>

####简要描述：
- requireVersion：1.0.0
- 描述：H5调用系统原生toast


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|info |是  |string | 需要提示的信息  |

####callBack：无

####调用接口示例：

```
widget.toast(info);
```  
***

###<font color="red">showDialog</font>

####简要说明：
- requireVersion：1.0.0
- 描述：H5调用系统原生dialog

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 提示框的title  |
|message |是  |string | 提示框的内容文本  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
|okBtn |是  |string | 确定Btn的文本  |
|cancelBtn |是  |string | 取消Btn的文本  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	

```
widget.showDialog(title,message,function(data){
	//data.type 0 取消 1 确定
},okBtn,cancelBtn);
```		
***

###<font color="red">alertDialog</font>

####简要描述：
- requireVersion：1.0.0
- 描述：H5调用系统原生dailog，显示效果类似alert

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 提示框的title  |
|message |是  |string | 提示框的内容文本  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
|okBtn |是  |string | 确定Btn的文本  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	

```
widget.showDialog(title,message,function(data){
	//data.type 1 确定
},okBtn);
```
***
###<font color="red">updateTitleBar</font>

####简要描述：
- requireVersion：2.4.0
- 控制header条

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|param |是  |json | 参数param{backAction:'checkChange',leftDisplay:false,leftText:'',leftAction:'checkChange',rightDisplay: true,rightText: '保存',rightAction: 'saveResume'}|


####callBack：无

####调用接口示例：	

```
widget.updateTitleBar(true);
```
***
###<font color="red">showPicker</font>

####简要描述：
- requireVersion：2.2.0
- 描述：调用通用select框

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | select框展示的数据 data {data1:[],data2:[]} data（数组）的个数代表列数  |
| select |否 |array | select框展示的默认值 数组的顺序代表为相应列数的默认值  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值 data.data1 data.data2 |

####调用接口示例：	

```
widget.showPicker(data,select,function(data){
	//data.data1 有几列，返回几个值
});
```

####修改记录:
|修改记录|version | requireVersion|作者|时间|
|:----   |:--- |:---|:----- |-----   |
|添加默认选择参数select |1.0.7|2.4.0  |李勇 | 2016.4.8  |

***

###<font color="red">callBrowser</font>

####简要描述：
- requireVersion：安卓 2.3.0
- 描述：调用系统浏览器

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|visitUrl |是  |string |  要跳转的链接 |


####callBack：无

####调用接口示例：

```
widget.callBrowser(visitUrl);
```
***
###<font color="red">showTimeRangePicker</font>

####简要描述：
- requireVersion：3.7.0
- 描述：选择时间

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|startTime |是  |string |  开始时间 |
|endTime |是  |string |  结束时间 |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：

```
widget.showTimeRangePicker(startTime, endTime, callBack);
```
***
