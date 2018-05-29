# 斗米C端 dek升级说明
>dek升级需要将新dek包及manifest说明文件上传至服务器进行dek升级，manifest说明文件(cache.manifest)中包括：

* Version：dek版本号
* RequiredVersion：app版本号（`用于标识哪些版本的app需求进行dek升级，高于此版本的app将进行升级`）
* Dek：dek名称 
* DekHash：dek加密代码
* CACHE：缓存
* NETWORK：网络配置

>请看cache.manifest长这样儿：

```
# Version: 2.2.7

# RequiredVersion:3.6.0

# Dek: main.dek

# DekHash: 7ce964d06c0a9d5a4cd6a78b454a4a95

CACHE:

NETWORK:
*
```

>其中，DekHash需要通过md5加密得到，如下：
```bash
$ md5 main.dek
MD5 (main.dek) = 7ce964d06c0a9d5a4cd6a78b454a4a95
```