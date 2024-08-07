# 统一框架设计

## 技术栈
采用SpringBoot生态

## 使用
1. 引入parent版本
```xml
<parent>
    <groupId>com.oceancode-cloud</groupId>
    <artifactId>oceancode-spring-boot-parent</artifactId>
    <version>${version}</version>
</parent>
```
指定version版本，目前支持`2.7.18`和`3.0.2`

2. 引入常用的依赖
```xml
<dependencies>
    <dependency>
        <groupId>com.oceancode-cloud</groupId>
        <artifactId>oceancode-common-web-spring-boot</artifactId>
    </dependency>

    <dependency>
        <groupId>org.mybatis.spring.boot</groupId>
        <artifactId>mybatis-spring-boot-starter</artifactId>
    </dependency>

    <dependency>
        <groupId>com.alibaba</groupId>
        <artifactId>druid-spring-boot-starter</artifactId>
    </dependency>

    <dependency>
        <groupId>com.mysql</groupId>
        <artifactId>mysql-connector-j</artifactId>
    </dependency>
</dependencies> 
```

