---
title: PicGo配置阿里云OSS
date: 2022-05-20 23:55:14
tags: 环境配置
---

# PicGo配置阿里云OSS

## 选购OSS产品

> 如果有账号直接登录，没有账号注册一个新的账号,登录阿里云之后选择产品→存储→对象存储OSS

点击直达：[阿里云对象存储](https://www.aliyun.com/product/oss?userCode=6if4uptj)

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled.png)

> 根据自己的需求选择资源包，标准包的价格也比较便宜半年不到五块钱。能满足基础需求后续有需要可以继续续费。

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%201.png)

## 创建存储容器

> 购买完成后进入控制台，进行对象存储管理

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%202.png)

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%203.png)

> 选择左侧Bucket列表，点击创建Bucket，填写名称，其他按照默认填写就行了。

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%204.png)

## 创建RAM子用户管理存储授权

> 建议使用RAM用户的AccessKey进行API的访问

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%205.png)

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%206.png)

> 创建一个RAM新用户，用于专门管理OSS存储。选择左侧的用户，然后点击创建用户，输入登录名称。确认无误之后提交

> ps：勾选Open Api调用，这样就会生成该用户的AccessKey ID 和 AccessKey Secret用于后续配置PicGo

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%207.png)

> 创建完成后记得保存你的AccessKey ID 和 AccessKey Secret,建议下载CSV文件。返回上一页之后就看不到了

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%208.png)

> 回到用户页，为新创建的用户添加权限。按如下所示进行权限的配置。

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%209.png)

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%2010.png)

## 配置PicGo

> 下载PicGo，下载链接：https://molunerfinn.com/PicGo/

> - keyId和KeySecret就是AccessKey ID 和 AccessKey Secret

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%2011.png)

> 存储空间名称填写刚创建的Bucket资源名称

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%2012.png)

> 存储区域填写下面的地址

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%2013.png)

> 通过主页面上传图片验证

![Untitled](https://picgo-xuexueli.oss-cn-beijing.aliyuncs.com/images/Untitled%2014.png)
