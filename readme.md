# Spring-boot基础包

Spring-boot基础包，为其它项目服务。

SpringBoot版本：2.0.2.RELEASE

此项目版本：1.0.0-RELEASE 持续更新中......

## 使用

其它项目在Maven中这样使用

```mxml
<!--spring-boot基础包，自己定义的-->
<dependency>
    <groupId>com.leigq.common</groupId>
    <artifactId>springboot-common</artifactId>
    <version>${springboot-common.version}</version>
</dependency>
```

## 包含内容

### 1、相关依赖：

```mxml
<!--starter-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
</dependency>

<!--web-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>

<!--lombok-->
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
</dependency>

<!--test-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
</dependency>

<!--编写更少量的代码：使用apache commons工具类库:
https://www.cnblogs.com/ITtangtang/p/3966955.html-->
<!--apache.commons.lang3-->
<dependency>
    <groupId>org.apache.commons</groupId>
    <artifactId>commons-lang3</artifactId>
</dependency>

<!--你可以把这个工具看成是java.util的扩展-->
<dependency>
    <groupId>org.apache.commons</groupId>
    <artifactId>commons-collections4</artifactId>
    <version>${commons-collections4.version}</version>
</dependency>

<!--apache.codec:编码方法的工具类包
https://blog.csdn.net/u012881904/article/details/52767853-->
<dependency>
    <groupId>commons-codec</groupId>
    <artifactId>commons-codec</artifactId>
</dependency>

<dependency>
    <groupId>org.apache.httpcomponents</groupId>
    <artifactId>httpclient</artifactId>
</dependency>

<!--commons-io-->
<dependency>
    <groupId>commons-io</groupId>
    <artifactId>commons-io</artifactId>
    <version>${commons-io.version}</version>
</dependency>
```

### 2、相关工具类及bean

- com.leigq.common.springboot

    - bean
        - BaseEntity

            基础实体类，其它实体继承此实体，此实体包含以下属性：
            
            ```java
            private Long id;
            
            private Date createTime;
            
            private Date updateTime;
            ```

        - Response

            统一响应对象。包含处理结果（Meta）和返回数据（Data）两部分，在 Controller 处理完请求后将此对象转换成 json 返回给前台。

    - util
        - RandomUtils

            生成随机数工具类

        - ValidateUtils

            验证工具类