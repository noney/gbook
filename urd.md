# URD 查询

## URD协议规则
	不区分大小写
	
	调用形式
	doumi://action/path?param=1&param1=2.......
		
	doumi://
	协议头部分,表示斗米产品调用
	
	action
	动作部分，用于表示客户端调起后，具体跳转到哪个页面或者具体执行哪些动作
	
	path
	用于表示当前的具体资源，支持url、实际的相对路径、虚拟路径。


## URD公共参数
~~~
urd公共参数：urdData（非必须，如果传就需要encode）

example：
	doumi://jobdetail?urdData=encodeURIComponent(a=1&b=2)
	或者
	doumi://jobdetail?job_id=xxx&urdData=encodeURIComponent(a=1&b=2)

A/B 测试参数：ad_test (非必须，值为1或2)

example：
	doumi://jobdetail?ab_test=1
~~~

## 通用框

| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 第三方页面<font style="color:red">（https）</font>							| url|	browser|external=1跳转到外部浏览器|encodeURIComponent(url)第三方连接需要编码|
| 第三方页面<font style="color:red">（http）</font>							| url|	link||encodeURIComponent(url)第三方连接需要编码|

## 登陆/注册

| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 登录（废弃）							| login.html|	login|||
| 重置密码 							| reset.html|	reset|||
| 注册 								| register.html|	register|||
| 验证码登录 							| login-captcha.html|	login-captcha|||
| 密码登录 							| login-password.html|	login-password|phoneNum||
| 第三方登录绑定手机号 					| login-check-phone.html|	login-check-phone|||
| 无法获取验证码 					| no-idencode.html|	no-idencode|||
| 更换手机号 					| change-mobile-number.html|	change-mobile-number|||
| 服务协议 					| agreement.html|	agreement||&nbsp;|


## 主tab页面

| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|  主tab页面（首页，特工，消息，个人中心）							| （index-new.html(<v3.5.0版本为index.html),online-index.html,native,account.html）|	jianzhimain|main_index <br />0 首页 <br />1 特工<br /> 2 消息 <br />3 个人中心|由于特工在首次安装客户端时候不存在，这时1代表消息tab,2代表个人中心|


##消息列表
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 系统通知		|msg-sys-list.html|jobmsglist	|messageType |消息类型|
| 章鱼小妹		|msg-operations-list.html|operationsmsglist	| messageType ||
| 偏好消息		|msg-preference-list.html|userpreferencelist	| messageType ||
| 附近兼职		|msg-nearby-list.html|nearbyjoblist	| messageType |&nbsp;|

##消息列表(新版)
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 工作邀约		|msg-invite-list.html|msg-invite-list	| messageType ||
| 特工通知		|msg-online-list.html|msg-online-list	| messageType ||
| 章鱼资讯		|msg-news-list.html|msg-news-list	| messageType |&nbsp;|

##特工
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 特工详情页		|online-detail.html|online-detail	|city _ id,task _ id ||
| 特工提交页面		|online-submit.html|online-submit	| ||
| 特工提交详情页面		|online-submit-detail.html|online-submit-detail	|apply _ id<br />task _ id<br />city _ id<br />post _ title<br />from=tsyfk（埋点） ||
| 特工重审		|online-retrial.html|online-retrial	|apply _ id<br />task _ id<br />post _ title ||
| 特工投诉		|online-complain.html|online-complain	|task _ id<br />from=submit_detai<br />post_title<br />status_str（帖子状态文字描述，例如已结束）||
| 选择特工投诉列表页		|online-complain-select.html|online-complain-select	||入口：投诉与反馈|
| 特工专区（目前只有斗米优选）	|online-prefecture.html|online-prefecture	|from<br />imageUrl||
| 特工提交成功页面		|online_submit-success.html|doumi:////modules/new_frame/online-submit-success.html	|hours,task_type ||
| 特工收入页面		|ol_income.html|onlineincome	|buttonTitle=去我的钱包 ||
| 我的特工页面		|online_personal.html|myonlinetask	|title = encodeURIComponent("我的特工")<br>subtitle = encodeURIComponent("全部,进行中,审核中,已结束")<br /> index|&nbsp;|

##淘宝客
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 淘宝客首页		|taobaoke-index.html|taobaoke-index	| ||
| 淘宝客收入		|taobaoke-income.html|taobaoke-income	| ||
| 淘宝客订单		|taobaoke-order.html|taobaoke-order	| ||
| 淘宝客搜索结果		|taobaoke-search.html|taobaoke-search	| ||
| 淘宝客搜索热词		|taobaoke-search-hot-key.html|taobaoke-search-hot-key	| ||
| 淘宝客分享		|taobaoke-share.html|taobaoke-share	| |&nbsp;|


## 详情页

| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 详情页							| detail.html|	jobdetail|job_id（帖子id）<br />  urdData（公共参数）| title(标题) <br /> hire_number(剩余可报名人数) <br /> payment _ type_str(结算方式，日结等)<br /> salary(工资)<br /> salary _ type _ str (工资单位) <br /> is_deposit(企业担保)<br /> has _ subsidy(有提成)<br /> cooperation_type(工资担保)<br /> ad _ types(商业标签)|
| 公司详情页							| company-detail.html|company-detail	|company_id（公司id）<br />  urdData（公共参数）<br /> company_logo（公司logo）|
| 全部工作地点							| detail-address.html|detail-address	|||
| 急速报名页面							| rapidly-apply.html|rapidly	| ||
| 报名成功页面							| apply-success.html|applysuccess	| ||
| 报名详情页面							| apply-detail.html|apply-detail	| ||
| 详情页工作地点页面							| detail-address.html|	doumi:///detail-address.html|post_id |&nbsp;|

## 列表页，专区页面
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
| 列表页							| list.html|joblist	|key=special_job<br>value=2 |筛选条件|
| 专区页							| prefecture.html|prefecture	|key=hot_post<br />value=1<br />urdData=imageUrl%3Dhttps%3A%2F%2Fcdn.doumistatic.com%2F18%2C2dfd7919fcff31.jpg%26log%3Dxsjz<br />hideFilter=0 |urdData包括imageUrl(专区头图)和log(专区统计字段)<br /> hideFilter: 0//默认显示 （ 0或空：显示，1:不显示)|
| 附近兼职列表页							| nearby-list.html|nearby-list	| ||
| 首页-为你优选-更多列表页					| selectiveperfect-list.html|selectiveperfect-list	| ||
| 首页-大家都在找-标签列表页				| hotjob-list.html|hotjob-list	| tag,title||
| 首页-完善简历页							| perfect-resume.html|perfect-resume	| ||
| 推荐列表							| recommend-list.html|recommend-list	| |&nbsp;|


## 积分相关
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|积分商城						| duiba.html|duiba	| ||
|签到成功页面						| sign-in.html|signsuccess	|message |签到提醒|
|赚积分页面						| earn-score.html|earnscore	| |v2.9.0|
|积分详情页面						| integral-detail.html|integraldetail	|total_score |积分总数|


## 个人中心
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|我的兼职						| apply-list.html|applylist	|title=encodeURIComponent("我的兼职")<br />subtitle=encodeURIComponent("全部,已报名,已录取,已结束") <br> index<br />entry(区分入口)|登录拦截，未登录跳login页面|
|投诉页面					| complain.html|complain	| id(帖子id)<br>status(帖子状态)<br>status_str(帖子状态文案)|登录拦截，未登录跳login页面|
|我的简历					| resume-index.html|resume-index| |登录拦截，未登录跳login页面|
|工作经历					| resume-work.html|resume-work| ||
|求职偏好					| resume-preference.html|resume-preference| ||
|教育经历					| resume-education.html|resume-education	| ||
|详细信息					| resume-addition.html|resume-addition	| ||
|基本信息					| resume-info.html|resume-info	| ||
|我的偏好						| preferences.html|userpreferences	| ||
|我的任务						| online-personal.html|useronline-personal	| ||
|我的收藏					| favorite.html|favorite	| |登录拦截，未登录跳login页面|
|邀友赚钱					| offline-share.html|offlineshare	| |登录拦截，未登录跳login页面|
|我的邀约					| offline-invite-list.html|offlineinvitelist	| |登录拦截，未登录跳login页面|
|我的分红					| offline-invite-bonus.html|offlineinvitebonus	| |登录拦截，未登录跳login页面|
|意见反馈					| feedback.html|feedback	| |登录拦截，未登录跳login页面|
|设置					| settings.html|settings	| |登录拦截，未登录跳login页面|
|投诉与反馈					| complain-and-feedback.html|complain-and-feedback	| |登录拦截，未登录跳login页面|
|斗米慧眼	首页				| huiyan-index.html|huiyan-index	| ||
|斗米慧眼	结果页				| huiyan-result.html|huiyan-result	| lat（经度）<br />lng（纬度）<br />address（地址）<br />city（城市名称）<br />district（区域名称）||
|社交账号绑定					| account-bind-list.html|account-bind-list	| |登录拦截，未登录跳login页面|
|设置成功					| set-resume-success.html|set-resume-success	| |登录拦截，未登录跳login页面|
|选择期望职位					| preferences-job-type-select.html|preferences-job-type-select	| |登录拦截，未登录跳login页面|

## 钱包
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|钱包页面					| wallet.html|userwallet	| |登录拦截，未登录跳login页面|
|提现页面					| applycash.html|applycash	| |登录拦截，未登录跳login页面|
|绑定微信					| bind-weixinwallet.html|bindweixinwallet	| |登录拦截，未登录跳login页面|
|绑定银行卡					| bind-unionpay.html|bindunionpay	| |登录拦截，未登录跳login页面|
|绑定支付宝					| bind-alipay.html|bindalipay	| |登录拦截，未登录跳login页面|
|提现记录					| apply-cash-record.html|apply-cash-record	| |登录拦截，未登录跳login页面|
|提现成功					| apply-cash-success.html|apply-cash-success	| |登录拦截，未登录跳login页面|
|提现申请					| apply-cash.html|apply-cash	| |登录拦截，未登录跳login页面|
|我的收入					| online-income.html|online-income	| |登录拦截，未登录跳login页面|

## 职位相关
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|待评价					| evaluate.html|evaluate	| | |
|选择城市					| city.html|city	| | |
|搜索					| serach.html|serach	| |&nbsp;|

## 公司信息
| 页面名称  | H5文件名称 | 对应urd|参数|备注|
| ------------- | ---------------------	| ---------------------|---------------------|---------------------|
|斗米慧眼					| huiyan-index.html|huiyan-index	| ||
|查询结果					| huiyan-result.html|huiyan-result	| |&nbsp;|

## &nbsp;
