# 斗米C端H5 DEBUG说明

>调试前，请先启动本地服务，如在命令行输入：
```bash
$ grain server
```

## IOS debug 调试
### 工具
IOS使用debug包自带的调试设置面板进行debug调试，因此需要安装带debug调试设置面板的debug包。

### 使用
* 1、打开debug调试设置面板
* 2、选择APP服务器环境（`test、sim、online`）
* 3、设置H5远程IP+PORT，如：`IP：10.216。102.102`，`PORT：8000`
* 4、设置需要调试的页面的URD，并选择启用，如：URD：`taskdetail`
* 5、设置该URD对应的PATH，如：`app/detail/detail/html`
* 6、以上信息设置完毕后，每个页面设置项的下方会显示完整URL，如：URL：`http://10.216.1010.216.102.102:8000/app/detail/detail/html`
* 7、可以点击【+】按钮，添加设置多个页面
* 8、最后，点击右上角【保存】按钮使设置生效

## Android debug 调试
### 工具
Android使用dmtools工具来进行debug调试，因此请在本机安装dmtools工具（[下载工具](http://framework.doumivip.com/)）。

### doumi tool
* 在终端打开指定url的页面；
* 在终端打开指定urd的页面；
* 更新终端上的dek。

### 使用
#### 调试指定url
* 1、输入远程IP地址+PORT+PATH，如：`http://10.216.1010.216.102.102:8000/app/detail/detail/html`
* 2、打开终端上APP相对应的页面，如职位详情页
* 3、点击【发送当前路径】，APP相对应的页面将刷新成远程URL对应的页面
* 4、打开`Chrome ADB Plugin`（需翻墙）中的`View Inspection Targets`选项，查看需要debug的页面

#### 调试指定urd
* 1、输入指定urd，如：URD：`taskdetail`
* 2、打开终端上APP相对应的页面，如职位详情页
* 3、点击【发送urd】，APP相对应的页面将刷新成远程URL对应的页面
* 4、打开`Chrome ADB Plugin`（需翻墙）中的`View Inspection Targets`选项，查看需要debug的页面

#### 更新dek
* 1、点击【选择dek文件】按钮，选择想要的dek后，将显示dek完整地址
* 2、点击【更新dek】按钮，APP将提示`update success`