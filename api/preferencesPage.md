#preferencesPage
```
H5:"preferencesPage.js"
nativeCls: "preferencesPage"
```

##接口变化：
```
新增
```

##详细接口：

###<font color='red'>showProvinceAndCityPicker</font>

####简要说明：
- requireVersion：2.7.5
- 描述：调用客户端控件获取省市区



####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string |  控件title |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：

```
preferencesPage. showProvinceAndCityPicker(title,function(data){
	// data.selected  数组   length 3  分别是省 市 区（ json ）id name
});
```
***


###<font color='red'>getExpectJobList</font>

####简要说明：
- requireVersion：2.7.5
- 描述：获取客户端首页存取的职位类型



####参数:无


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：

```
preferencesPage. showProvinceAndCityPicker(title,function(data){
	console.log(data.data); //data.data 数组
              {
                  choice_type: 1
                  count: "836"
     	           field: "job_type"
                  filter_category_name: "职位类型"
                  name: "不限" // 职位类型
                  value: "0"   // 职位类型ID
      		 }
});
```
***




###<font color='red'>setPreferencesSuccess</font>

####简要说明：
- requireVersion：2.7.5
- 描述：通知客户端偏好设置保存成功，控制IM里面的偏好设置入口



####参数:无


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|isSuccess |是  |number | 1 成功 0 失败 |

####调用接口示例：

```
preferencesPage. setPreferencesSuccess(isSuccess);
```
***