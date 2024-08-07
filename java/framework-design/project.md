# 工程开发设计

## 目录结构
此目录结构为自动生成的目录，无需手动修改
```text
|--common 公共模块
   |--config
      |--handler 数据层使用的枚举自定义Handler
   |--datasource 数据源配置目录
|--controller 接口目录
   |-- ApiController 新增，删除，修改接口Controller
   |-- QueryFunctionController 查询接口
   |-- QueryFunctionImpl graphql查询接口
|--function 函数模块
|--mapper Mapper 目录
|--model 模型目录
|--repository 数据库操作实现
|--service Service模块
|--util 工具类目录
|--MainApp 入口启动文件
|--resources 资源目录
   |--repository Mapper对应的xml文件
```

## 工具类
### ValueUtil
用于业务字段的工具类，几乎覆盖大部分场景。

1. isEmpty  各种类型空判断
2. isNotEmpty 各种类型非空判断
3. isTrue 布尔类型true判断
4. isFalse 布尔类型false判断
5. isEquals 各种类型比较

### SessionUtil
业务字段，登录用户id工具类

## 异常处理
业务异常使用`BusinessRuntimeException`，会统一进行处理：
1. 客户端异常会返回给用户，并适配对应的http响应码。
2. 服务端异常会进行日志记录。
3. 常用错误码可用`CommonErrorCode`中已经定义的，也可自行扩展。

## 接口开发
通过定义函数形态，会自动生成对应类型的接口。本框架接口分未两类：
1. 查询类：查询类接口统一使用graphql进行组合使用。
2. 新增，删除，修改类接口使用`Restfull`接口

> 接口的环境框架本身已集成，开发者无需关心直接使用即可

## 接口调用
Restfull接口： `/api/XXX/XXX`,定义在`ApiController.java`中

Graphql接口：`/api/graphql/query`，定义在QueryFunctionController.java中
