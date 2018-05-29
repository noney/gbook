#clientUI
```
H5:"clientUI"
nativeCls:"clientUI"
```

##接口变化：
```
删除：
	- showApplyCashResultDialog 
	- showEnrollSuccessDialog 

迁移：	
	- showCityPicker  clientUI→cityApi(2.7.5)

更改：
	-showDialog(2.8.0)
```

##详细接口：

###<font color="red">showCaptchaDialog</font>

####简要描述：
- requireVersion：2.3.0
- 描述：调用客户端定制图片验证码框

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 定制框的title  |
|img |是  |string | img 图片(base64)  |
|times |是  |number | 次数 依据次数来判断首次加载，还是第二次及更多次加载  1 显示整个框 2 只替换图片  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
clientUI.showCaptchaDialog(title,img,function(data){
	data.status==1; //确定 data.status==0 取消 然后执行不同函数
   	data.code=xxxx;  //用户填写的验证码
})
```
***

###<font color="red">bigPicturePreview</font>

####简要描述：
- requireVersion：2.4.0
- 描述：大图预览接口

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 标题  |
|imgs |是  |array |图片链接组成的数组 |
|index |是  |number | 图片索引 |


####callBack：无

####调用接口示例：	
```
clientUI.bigPicturePreview(title, imgs, index)
```
***

###<font color="red">pictureOperationDialog</font>

####简要描述：
- requireVersion：2.4.0
- 描述：图片操作弹层

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 标题  |
|imgs |是  |array | 大图链接数组 |
|index |是  |number | 图片位置 |
|callback |是  |function | 用户点删除时候执行的回调函数|


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
clientUI.pictureOperationDialog(title, imgs, index, function(){
	     // 当用户点击"删除"按钮的时候会回调执行该函数
})
```
***

###<font color="red">selectImage</font>

####简要描述：
- requireVersion：2.4.0
- 描述：调用客户端选择图片控件

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|isEdit |是  |number | 是否可裁剪，0不要裁剪，1可裁剪，不传此参数默认可裁剪  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| imgData |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
clientUI.selectImageDialog(function(imgData){
     imgData.base64ImageData // 图片的base64数据 ios
     imgData.localImageUrl // 本地图片路径 Android
 })
```
***

###<font color="red">uploadImage</font>

####简要描述：
- requireVersion：2.4.0
- 描述：调用客户端上传图片控件

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|fileData |是  |string | 图片的base64数据 或 图片的本地url  |
|isEdit |是  |boolean | 是否可裁剪，0不要裁剪，1可裁剪，不传此参数默认可裁剪  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| urlJson |是  |string | 图片上传后的服务器端url  |

####调用接口示例：	
```
clientUI.uploadImage(param, function(url){
     // 是图片上传后的服务器端url
 })
```
***

###<font color="red">selectAndUploadImage</font>

####简要描述：
- requireVersion：2.4.0
- 描述：调用客户端选择图片并上传

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|isEdit |是  |boolean | 是否可裁剪，0不要裁剪，1可裁剪，不传此参数默认可裁剪  |
|type |是  |number | 上传类型。1特工任务提交截图，2修改头像，3我的简历-个人照片  |
|callback |是  |function | 点击删除按钮的回调函数  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 图片上传后的图片对象  |

####调用接口示例：	
```
clientUI.selectAndUploadImage(function(data){
	data.imageURL 图片服务器地址	
	data.imageName 图片名称
 },0,1)
```
***
###<font color="red">showDialog</font>

####简要说明：
- requireVersion：2.8.0
- 描述：H5调用定制dialog

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 提示框的title  |
|message |是  |string | 提示框的内容文本  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |
|okBtn |是  |string | 确定Btn的文本  |
|cancelBtn |是  |string | 取消Btn的文本  |
|imageName |否  |string | 通知客户端显示不同的定制图片，不传显示默认  |
|titleAttribute |否  |array | 更改弹窗title中部分字符串颜色  |
|messageAttribute |否  | array | 更改弹窗message中部分字符串颜色  |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
widget.showDialog(title,message,function(data){
	//data.status 0 取消 1 确定
},okBtn,cancelBtn,imageName,titleAttribute,messageAttribute);

{//新增字段数据结构
	titleAttribute: [ // 标题文字样式
		{
			location: 0, //开始位置
			length: 3, //从开始位置起的字符个数
			color: #000000 //对应的颜色
		},
		{
			location: 3,
			length: 3
			color: #234234
		}	
	],
 	messsageAttribute: //消息文字样式
 	[
 		{
 			location: 0,
 			length: 3,
 			color: #000000
 		}
 	]
}
```	
####修改记录:
|修改记录|version | requireVersion|作者|时间|
|:----   |:--- |:---|:----- |-----   |
|添加imageName字段，通知客户端需要显示的图片|1.0.8|2.4.0  |李勇 | 2016.4.14 |
	
***


###<font color="red">showPicker</font>

####简要说明：
- requireVersion：2.4.0
- 描述：H5调起通用select框

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|param |是  |json | {data1:[],data2:[]}  |
|select |是  |array | ['0','1']  默认值,'0' 为默认值的位置，字符串  |
|title |是  |string | 标题  |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
widget.showPicker(param,select,title,function(data){
	//data.data1 返回的选择的值的index
	//data.data2 返回的选择的值的第二列的index
});
```	
***

###<font color="red">showMultiPicker</font>

####简要说明：
- requireVersion：2.4.0
- 描述：H5调起通用select多选框

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 多选框的标题  |
|param |是  |array | [[0,1],[1,2]] 多选默认值,0 为默认值的位置，number  多维数组 单列也是 |
|select |是  |array | ['0','1']  默认值,'0' 为默认值的位置，字符串  |
| maxSelect |否  |Number | 3 最多可筛选几项  |

####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
widget. showMultiPicker(title,select,param,function(data){
	//多维数组
},maxSelect);
```	
***


###<font color="red">alertDialog</font>

####简要描述：
- requireVersion：2.3.0
- 描述：H5调用定制dailog，显示效果类似alert

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
	//data.status 1 确定
},okBtn);
```
***

###<font color="red">copyDialog</font>

####简要描述：
- requireVersion：2.4.0
- 描述：H5调用定制dailog，复制联系人信息

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 提示框的title  |
|subtitle |是  |string | 需要复制的内容文本  |
|detail |是  |string | 对复制文本的描述  |
|confirmButton |是  |string | 操作按钮的文本  |
|cancelButton |否  |string | 取消Btn的文本  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
widget.copyDialog(title, subtitle , detail, confirmButton , cancelButton ,function(data){
	//data.status 1 确定
},okBtn);
```
***

###<font color="red">showPhoneDialog</font>

####简要说明：
- requireVersion：2.4.0
- 描述：H5调用定制打电话dialog

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 提示框的title  |
|message |是  |string | 电话文本  |
|okBtn |是  |string | 确定Btn的文本  |
|cancelBtn |是  |string | 取消Btn的文本  |
|imageName |否  |string | 通知客户端显示不同的定制图片，不传显示默认  |
|callBack |是  |function | 回调函数 通信完成之后需要执行的函数  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
widget.showPhoneDialog(title,message,function(data){
	//data.status 0 取消 1 确定
},okBtn,cancelBtn);
```	
***

###<font color="red">setBannerView</font>

####简要说明：
- requireVersion：2.7.0
- 描述：调用客户端轮播图

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|x |是  |number | 左上角坐标  |
|y |是  |number | 左上角坐标  |
|height |是  |number | 轮播图的高度 |
|data |是  |json | 给客户端传服务端返回数据 |


####callBack：
无

####调用接口示例：	
```
clientUI. setBannerView(0,0,height,data);

data结构：
	{
		"1": {
			"id": 9,
			"title": "\u6597\u7c73\u5e97\u5c0f\u4e8c",
			"image": "http:\/\/sta.doumistatic.com\/src\/image\/jianzhi\/mobile\/c\/app\/v2\/catering\/banner_canyin_app.jpg",
			"url": "http:\/\/m.doumi.com\/pinpai\/canyin\/?ca_name=dm&ca_campaign=ppcy",
			"active_sdate": "",
			"active_edate": "",
			"active_city_ids": "13,12,27,26,194,28,75,67"
		},
		"3": {
			"id": 4,
			"title": "\u6597\u7c73\u7279\u5de5",
			"image": "http:\/\/sta.doumistatic.com\/src\/image\/jianzhi\/mobile\/banner\/banner_tegong_app.jpg",
			"url": "http:\/\/m.doumi.com\/tegong.htm?ca_name=doumi&ca_source=wap&ca_from=sybanner",
			"active_sdate": "",
			"active_edate": "",
			"active_city_ids": "0"
		}
	} 
```	
***



###<font color="red">invokeCamera</font>

####简要描述：
- requireVersion：2.7.5
- 描述：H5只调用客户端相机

####参数:
无


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
clientUI.invokeCamera(function(data){
		//{status: "1", imageURL: "17,2822e4954e5811.png@base@tag=imgScale&h=&w="} 
		// 需要拼接 https://image.doumi.com/
		
        //{status: "0"}
});
```
***


###<font color="red">showContactDialog</font>

####简要描述：
- requireVersion：2.9.0
- 描述：显示联系方式选项框

####参数:
无


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|data |是  |object | 客户端执行回调时的返回值  |

####调用接口示例：	
```
clientUI.showContactDialog(buttonTitle_1, buttonTitle_2, function(data){
		//{status: "0"} 取消
        //{status: "1"} IM 
        //{status: "2"} 其他方式联系商家
});
```
***



###<font color="red">uploadPrivateImage</font>

####简要描述：
- requireVersion：3.0.0
- 描述：调用客户端选择图片并上传

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|isEdit |是  |boolean | 是否可裁剪，0不要裁剪，1可裁剪，不传此参数默认可裁剪  |
|callback |是  |function | 点击删除按钮的回调函数  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| imgUrl |是  |string | 图片上传后的服务器端url

####调用接口示例：	
```
clientUI.uploadPrivateImage(function(imgUrl){

 });
```
***


###<font color="red">showCaptcha2Dialog</font>

####简要描述：
- requireVersion：3.1.0
- 描述：调用客户端定制图片验证码框

####参数:
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|title |是  |string | 标题  |
|mobile |是  |string | 手机号  |
|keyboard |否  |string | default或不传或为空  全键盘，number  数字键盘 |
|type |否  |string | 1为登录注册, 2更换手机号, 不传默认为1 |
|callback |是  |function | 点击按钮的回调函数  |


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| data |是  |object | 客户端执行回调时的返回值

####调用接口示例：	
```
clientUI.showCaptcha2Dialog(function(data){
    data.status=1; 1 成功 0 取消按钮
 });
```
***


###<font color="red">getCustomerServicePhoneNumbers</font>

####简要描述：
- requireVersion：3.7.0
- 描述：调用客户端下发的客服电话

####参数: 无


####callBack：
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| tel |是  |object | 客户端执行回调时的返回值

####调用接口示例：	
```
clientUI.getCustomerServicePhoneNumbers(function(tel){
    tel.service_phone = 400-733-3300; 返回对象 里面 service_phone 字段是客服电话
 });
```
***