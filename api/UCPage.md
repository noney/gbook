#UCPage
```
H5:"UCPage"
nativeCls:"UCPage"
```

##接口变化：
```
userCenterApi拆分成UCApi、UCPage
	移动：
		- stashChangeOfApplist （UCApi→UCPage）
		- resumeComplete	 （UCApi→UCPage）
```

##详细接口：

###<font color="red">stashChangeOfApplyList</font>
####简要说明：
- requireVersion：2.4.0
- 描述：暂存取消帖子索引


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|option |是  |string | 添加还是移除 add代表添加 remove代表移除  |
|pushData |是  |number | 帖子Id|

####callBack：无


####调用接口示例：

```
UCPage.stashChangeOfApplyList(option, postId);
```
***
###<font color="red">resumeComplete</font>
####简要说明：
- requireVersion：2.4.0
- 描述：通知简历状态


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|status |是  |boolean | 状态  |

####callBack：无


####调用接口示例：

```
UCPage.resumeComplete(status);
```
***

###<font color="red">comment</font>
####简要说明：
- requireVersion：3.7.0
- 描述：把信息提交给评价窗口展示


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 职位名称  |
|corp_name |是  |string | 公司名称 |
|is_company_certified |是  |boolean | 是否认证  |
|post_id |是  |number | 职位ID  |
| post_user_id |是  |number | 商家id  |
| company_id |是  |number | 公司id |
| listing_status |是  |number | 报名状态 |
| from |是  |number | 来源tab |
| show_status_str |是  |string | 状态字符串 |

####callBack：无

####调用接口示例：

```
UCPage.comment(title, corp_name, is_company_certified, post_id, post_user_id, company_id, listing_status, from, show_status_str);
```
***

###<font color="red">resumeComplete</font>
####简要说明：
- requireVersion：3.7.0
- 描述：通知简历状态


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|status |是  |boolean | 状态  |
|resumeCredit |是  |string | 1完善基本信息，2完善全部简历信息 |

####callBack：无

####调用接口示例：

```
UCPage.resumeComplete(status, resumeCredit);
```
***