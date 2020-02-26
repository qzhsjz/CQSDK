


# CQSDK
- 下载即用,极速上手
- 不含有任何编程依赖(运行需要环境)
- 在事件里,e对象提供你想要的任何操作
- 基于VC++
- 基于官方SDK 9.25
- **自主知识产权**

## 上手指南
1. [下载](https://github.com/MikuPy2001/CQSDK/releases)
2. 打开CQAPP.sln
3. 用力点击编译按钮生成插件

## 环境要求
- VS2019
- Windows SDK
- 平台工具集(v142)

VS2015/VS2017未做兼容测试,但是应该可以

## 如何开始编写插件
- 推荐直接查看appinfo.h跟着源码注释阅读
- 全部阅读并**根据提示修改**完毕后就可以尝试生成

## 如何部署插件
- SDK已经集成了部署工具CQJSON,编译即可完成部署
- 如不使用,请按以下步骤进行部署
- 1. 打开app.json
- 2. 根据你的代码,按照json提供的注释,填写所有字段,删除多余字段

## 参考文献
- 你可以在[这里](https://mikupy2001.github.io/cqsdk-help/ "DOCS")查看SDK全部函数和类,以及帮助

## 高级

>有的人会问:教练!VS好大,装不起啊,window SDK我也没有啊,平台工具集是个什么鬼啊.
>
>那太棒了,这里喵将会引导你如何使用你惯用的构建工具构建项目

### **前提**
你所使用的构建工具至少要支持以下2点
- C++11
- std

>喵认为只要不是上个世纪的构建工具,应该都支持.

### **知识点**

>简单一点喵!

现在,你只需要知道SDK所包含的目录分别是干什么的就大功告成啦.

|目录名称|用途|
|-|-|
|CQ_APP|这是项目源码目录,包含有示例项目|
|CQ_LIB|这是SDK预编译好的LIB,有发布版和debug版|
|CQ_SDK|这是SDK头文件|

### **最后**
>喵相信难不倒聪明的你的

你需要在你的构建工具中将以上三个目录有机组织一下,以便生成DLL

请生成名称为APP的DLL文件,这是酷Q的规定

### **扩充的内容**
本SDK提供了一个方便的工具用于分析源码生成插件所需的JSON,同时还能将生成的DLL和JSON发布到酷Q目录

>这么方便的工具你还不赶紧用起来喵!

使用方法如下

`CQ_Json.exe <源码目录> <DLL生成目录> (酷Q目录)`

**1.请不要将SDK头文件放入源码目录或将源码目录指向SDK目录**

**2.酷Q目录参数通常不是必须,且会被源码中的宏替换**

3.恭喜你看完了全部内容,赶紧开始写吧


----
## 历史归档(雨女无瓜)

当前目标

1. CQMsgCode 重写(现在这个版本它不香吗

2. winSpeak 继续支持(鸽了

3. 下列函数未有EX版本
    ```
    #define	EVE_GroupUpload(Name) 完成
    #define	EVE_System_GroupMemberDecrease(Name) 完成
    #define	EVE_System_GroupMemberIncrease(Name) 完成
    ```

4. 首页文档

5. 跟进到9.25 基本完成

5.1 API完善 完成

5.2 群事件-群禁言 完成

6 视频教程(鸽了
