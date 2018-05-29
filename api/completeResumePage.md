#completeResumePage
```
H5:"completeResumePage"
nativeCls:"completeResumePage"
```

##接口变化：
```
3.0.0 新增，首页-完善简历数据统一由客户端管理
```

##详细接口：

###<font color="red">getResumeInfo</font>

####简要描述：
- requireVersion：3.0.0
- 描述：获取用户在引导页填写信息

####参数:
无
####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：
```
completeResumePage.getResumeInfo(function(data){ //1 完成 0 未完成 
    { //data 
        gender:1, //1 男 2 女
        identity:1, //1 学生 3 非学生
        birth:1990, //出生年份
        name:xxx, //姓名
    }
});
```
***