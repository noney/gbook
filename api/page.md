#page

```
page.js(模块继承类)
```

##接口变化：

```
	增加：
		- goBack （clientInfo→page）(参数变化 2.7.5)
		- dataDownloadFinished （clientInfo→page）
		- loadPageStatus （widget.loadState→page）
		- canPullWebView （widget.setPullToRefreshWebView→page）
		- getNavbarHeight （widget→page）
		- loadState （widget→page）
		- setPullToRefreshWebView （widget→page）
```
##详细接口：

```
page.js(模块继承类)
```

###<font color='red'>getOptions</font>
####简要描述:
- requireVersion：1.0.0
- 描述：从客户端获取参数

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####接口调用示例：
```
listApi.getOptions(function(data){
	console.log(data);
});
```
***

###<font color='red'>dataDownloadFinished</font>
####简要描述：
- requireVersion：1.0.0
- 描述：通知客户端数据加载完成

####参数：无

####callback：无

####接口调用示例：
```
indexPage.dataDownloadFinished();
```
***

###<font color='red'>listDataLoadFinished</font>
####简要描述：
- requireVersion：2.7.5
- 描述：通知客户端列表数据加载完成

####参数：无

####callback：无

####接口调用示例：
```
indexPage.dataDownloadFinished();
```
***

###<font color='red'>refreshPage</font>
####简要说明：
- requireVersion：2.5.0
- 描述：刷新页面

####参数：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|type |否  |number | 默认为1   这个参数透传给window.loadData(1); 这个时候H5调用getOptions重新获取参数（暂时没有用到）|

####callBack：无

####接口调用示例：
```
listApi.refreshPage(type);
```
***
###<font color="red">goBack</font>
####简要描述：
- requireVersion：2.2.0
- 返回上一级页面，同时根据参数判断是否要加载H5的window.loadData();在参数里面详细描述

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| isLoad |否 |number | 为1 客户端返回上一级页面，同时加载window.loadData(); 为0时不执行window.loadData(); 默认为0 |
| backIndex |否 |number | 一个id值，在getWebViewID中获取的，表示goback到id值的那个页面，不管中间存在多少页面 |
| dara |否  |string | encode过的字符串，返回到目标页面后，如果data不为空，则不管isLoad 是0还是1,则都会触发windows.loadData(data),并将data数据回传给h5 |

####callBack：无

####调用接口示例：
```
clientInfo.goBack(1);
```
***

###<font color='red'>loadPageStatus</font>
####简要描述：
- requireVersion：1.0.0
- 描述：通知客户端数据加载完成

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| status |是  |string | 需要显示的状态 loading  loadSuccess  loadFailed  noData  netWorkFailed |
| msg |是  |string | 页面文案显示 |

####callback：无

####接口调用示例：
```
indexPage.loadPageStatus();
```
***
###<font color="red">getNavbarHeight</font>

####简要说明：
- requireVersion 2.4.0
- 描述：ios获取顶部导航栏高度

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callBack |是  |Function | 回调函数 |


####callBack：无

####调用接口示例：

```
indexPage.getNavbarHeight(function(height){
    console.log(height)
});
```
***
###<font color="red">canPullWebView</font>

####简要说明：
- requireVersion 2.1.0
- 描述：ios获取顶部导航栏高度

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|canRefreshable |是  |boolean | 控制下拉刷新 |

####callBack：无

####调用接口示例：
```
indexPage.canPullWebView(true);
```
***

###<font color="red">domPosition</font>

####简要说明：
- requireVersion 2.6.0
- 描述：元素在页面当中的绝对位置和自己的高低，用于解决ios第三方键盘遮挡问题

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|top |是  |number | 元素距离页面顶端的位置 |
|height |是  |number | 元素的高度 |

####callBack：无

####调用接口示例：
```
indexPage. domPosition(top,height);
```
***

###<font color="red">updateTitleBar</font>

####简要描述：
- requireVersion：2.7.0
- 控制header条

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|param |是  |json | param{backAction:'checkChange',leftDisplay:false,leftText:'',leftAction:'checkChange',rightDisplay: true,rightText: '保存',rightAction: 'saveResume'}|


####callBack：无

####调用接口示例：	

```
index.updateTitleBar(param);   //之后补充应用场景
```
***

###<font color='red'>getWebViewID</font>
####简要描述:
- requireVersion：2.7.5
- 描述: 获取当前页面的唯一id值

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |Number | 获取当前页面的唯一id值  |

####接口调用示例：
```
listApi.getOptions(function(webviewID){
	console.log(webviewID); //0
});
```
***