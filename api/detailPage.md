#detailPage
```
H5:"detailPage"
nativeCls:"detailPage"
```

##接口变化：
```
detailApi → detailPage
删除：
	- getDetailData 
```

##详细接口：

###<font color="red">getCompanyData</font>

####简要描述：
- requireVersion：2.4.0
- 描述：向客户端获取发帖人的信息(联系人，联系方式)

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|jobId |否  |string | 职位Id,预留参数  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：
```
detailPage.getCompanyData(function(data){
   console.log(data.consulting); //商家所有联系方式
   //consulting: {
   				  "0":{"consulting_no":"15210641250","consulting_remark":"phone"}, //电话
                  "1":{"consulting_no":"","consulting_remark":""}, // 微信
                  "2":{"consulting_no":"","consulting_remark":""} //  QQ
                  "4":{"consulting_no":"","consulting_remark":""} //  公众账号                  
                  }
     console.log(data.contact_person); //商家联系人
});
```
***


###<font color="red">getLayoutParam</font>

####简要描述：
- requireVersion：2.6.5
- 描述：向客户端请求急速报名的所有限制信息

####参数:
无
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：
```
detailPage. getLayoutParam(function(data){

    job_id 
	job_type //工作类型
	is_login //是否已经登录
	is_resume_complete //简历是否完整
	extra_requirement //急速报名的限制条件
});
```
***

###<font color="red">submit</font>

####简要描述：
- requireVersion：2.6.5
- 描述：急速报名用户填写的数据提供给客户端，由客户端提交给服务端

####参数:
|data |是  |object | 用户填写的内容，详细见wiki  |
####callBack：
无

####调用接口示例：
```
detailPage.submit(data);
```
***