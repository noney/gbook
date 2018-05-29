#applyListPage
```
H5:"applyListPage"
nativeCls:"applyListPage"
```

###<font color="red">updateApply</font>
####简要说明：
- requireVersion：2.8.0
- 描述：通知客户端职位状态变了


####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|tab_index |是  |string | 当前tab索引  |
|post_opr |是  |object | 职位操作信息 |

####callBack：无

####调用接口示例：

```
applyListPage.updateApply(tab_index, post_opr);
```
***

###<font color="red">onlineConsultation</font>

####简要描述：
- requireVersion：3.7.0
- 通知客户端调用在线咨询

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| post_id |是  |number | 职位id|
| company_user_id |是  |number | 商家的id|
| post_name |是  |string | 职位名称|

####callBack：无

####调用接口示例：
```
applyListPage.onlineConsultation(post_id, company_user_id, post_name);
```
***
###<font color="red">cancelApply</font>

####简要描述：
- requireVersion：3.7.0
- 通知客户端发送取消请求

####参数：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| post_id |是  |number | 职位id|

####callBack：无

####调用接口示例：
```
applyListPage.cancelApply(post_id);
```
***

###<font color="red">updateJobListOver</font>

####简要描述：
- requireVersion：2.8.0
- 通知客户端列表已更新完成

####参数：无

####callBack：无

####调用接口示例：
```
applyListPage.updateJobListOver();
```
***
