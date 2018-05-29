#indexPage

```
H5:"indexPage.js"
nativeCls:"indexPage"
```

##接口变化：

```
 indexApi→indexPage
```

##详细接口：

###<font color="red">setFilterMenu</font>

####简要描述：
- requireVersion：2.6.0
- 描述：设置FilterMenu距离顶部的高度,顶部渐变导航条渐变的高度


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|height |是  |number | 设置filterMenu 的高度  |
|opacityHeight |是  |number | 设置渐变的高度  |
|sex |是  |string | 设置FilterMenu筛选项里面的性别  |
|identity |是  |string | 设置FilterMenu筛选项里面的身份  |
####callBack：无

####调用接口示例：
```
indexPage.setFilterMenu(height, opacityHeight, sex, identity)
```
***

###<font color="red">setFilterMenuForExplore</font>

####简要描述：
- requireVersion：3.1.0(IOS探索版)
- 描述：设置FilterMenu筛选项里面的性别和身份信息


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|sex |是  |string | 设置FilterMenu筛选项里面的性别  |
|identity |是  |string | 设置FilterMenu筛选项里面的身份  |
####callBack：无

####调用接口示例：
```
indexPage.setFilterMenuForExplore(sex, identity)
```
***

###<font color="red">clickFilterMenu</font>

####简要描述：
- requireVersion：2.6.0
- 描述：通知客户端用户点击H5FilterMenu(<font style="color:blue">安卓</font>)


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|index |是  |number | 通知客户端点击menu的位置  |
####callBack：无

####调用接口示例：
```
indexPage.clickFilterMenu(index)
```
***

###<font color="red">listDataLoadFinished</font>

####简要描述：
- requireVersion：2.6.0
- 描述：下拉刷新时通知客户端列表加载完成，滚动到顶(<font style="color:blue">安卓</font>)


####参数: 无
####callBack：无

####调用接口示例：
```
indexPage.listDataLoadFinished()
```
***


###<font color="red">hotKeyWords</font>

####简要描述：
- requireVersion：3.0.0
- 描述：设置搜索热词


####参数: 
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |array | 斗米直聘：跳转直聘页面，链接： https http ://m.doumi.com/zhipin /index/，职位订阅：app内职位订阅链接，每日任务：做任务赚积分页面链接，展会­­协助：点击出现职位list，学生专享：跳转学生专区，临时工：点击后搜索页面出现职位list，服务员：点击后搜索页面出现职位list，传单派发：点击后搜索页面出现职位list，家教助教：点击后搜索页面出现职位list  |
####callBack：无

####调用接口示例：
```
indexPage.hotKeyWords(
    [
        {
            "title": "斗米直聘",
            "urd": "doumi://browser/https://m.doumi.com/zhipin/index/"
        },
        {
            "title": "职位订阅",
            "urd": "doumi://userpreferences"
        },
        {
            "title": "展会协助",
            "urd": ""
        },
        {
            "title": "学生专享",
            "urd": "doumi://prefecture?key=hot_post&value=534&urdData=imageUrl%3Dhttps%3A%2F%2Fcdn.doumistatic.com%2F18%2C2dfd7919fcff31.jpg%26log%3Dxsjz"
        },
        {
            "title": "临时工",
            "urd": ""
        },
        {
            "title": "服务员",
            "urd": ""
        },
        {
            "title": "传单派发",
            "urd": ""
        },
        {
            "title": "家教助教",
            "urd": ""
        }
    ])
```
***

###<font color="red">getLocation</font>

####简要描述：
- requireVersion：探索版 3.1.0
- 描述：获取定位(<font style="color:blue">IOS探索版</font>)


####参数: 无
####callBack：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####调用接口示例：
```
indexPage.getLocation(function(data){
    data.lat //经度
    data.lon //纬度
}
```
***

###<font color="red">getFilterMenuBarHeight</font>

####简要描述：
- requireVersion：3.5.0
- 描述：获取筛选框高度(<font style="color:blue">安卓</font>)


####参数: 无
####callBack：

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 回调函数执行的返回值|

####调用接口示例：
```
indexPage.getFilterMenuBarHeight(function(data){
    data.bottomFilterMenuBarHeight //二级筛选框高度
    data.topFilterMenuBarHeight //一级筛选框高度
}
```
***
