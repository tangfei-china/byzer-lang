## MLSQL

MLSQL is a Programming Language designed For Big Data and AI, it also has a distributed runtime.

![](http://docs.mlsql.tech/upload_images/WechatIMG67.png)

## Official WebSite

[http://www.mlsql.tech](http://www.mlsql.tech)

Find more examples on [our user guide](http://docs.mlsql.tech/en).

1. [中文文档](http://docs.mlsql.tech/mlsql-stack/)
2. [English Docs](http://docs.mlsql.tech/en)

## <a id="Download"></a>Download MLSQL
* The lasted version is MLSQL v2.0.1
* You can download from [MLSQL Website](http://download.mlsql.tech/2.0.1/)
* Spark 2.4.3/3.0.0 are tested

***Naming conventions***

mlsql-engine_${spark_major_version}-${mlsql_version}.tgz
```shell
## Pre-built for Spark 2.4.x
mlsql-engine_2.4-2.1.0-SNAPSHOT.tar.gz 

## Pre-built for Spark 3.0.x           
mlsql-engine_3.0-2.1.0-SNAPSHOT.tar.gz  
```  

## <a id="Build"></a>Building a Distribution
### Prerequisites
- JDK 8+
- Maven
- Linux or MacOS

### Downloading Source Code
```shell
## Clone the code base
git clone https://github.com/allwefantasy/mlsql.git .
cd mlsql
```
### Building Spark 2.3.x Bundle
```shell
export MLSQL_SPARK_VERSION=2.3
./dev/make-distribution.sh
```
### Building Spark 2.4.x Bundle
```shell
export MLSQL_SPARK_VERSION=2.4
./dev/make-distribution.sh
```

### Building Spark 3.0.x Bundle
```shell
export MLSQL_SPARK_VERSION=3.0
./dev/make-distribution.sh
```
### Building without Chinese Analyzer
```shell
## Chinese analyzer is enabled by default.
export ENABLE_CHINESE_ANALYZER=false
./dev/make-distribution.sh <spark_version>
```
### Building with Aliyun OSS Support
```shell
## Aliyun OSS support is disabled by default
export OSS_ENABLE=true
./dev/make-distribution.sh <spark_version>
```

## Deploying
1. [Download](#Download) or [build a distribution](#Build) 
2. Install Spark and set environment variable SPARK_HOME
3. Deploy tgz
- Set environment variable MLSQL_HOME
- Copy distribution tar ball over and untar it
4.Start MLSQL in local mode
```shell
cd $MLSQL_HOME
## Run process in background
nohup ./bin/start-local.sh 2>&1 > ./local_mlsql.log &
```
5. Open a browser and type in http://localhost:9003, have fun.

## Contributing to MLSQL

If you are planning to contribute to this repository, please create an issue at [our Issue page](https://github.com/allwefantasy/streamingpro/issues)
even if the topic is not related to source code itself (e.g., documentation, new idea and proposal).

This is an active open source project for everyone,
and we are always open to people who want to use this system or contribute to it.


## Contributors

* Zhu William/allwefantasy#gmail.com
* Chen Fu/cfmcgrady#gmail.com
* Geng Yifei/pigeongeng#gmail.com
* wanp1989/wanp1989#126.com
* chenliang613
* RebieKong
* CoderOverflow
* ghsuzzy
* xubo245
* zhuohuwu0603
* liyubin117
* 9bbword
* Slash-Wong/523935329#qq.com
* anan0120/158989903#qq.com


----------
[![HitCount](http://hits.dwyl.io/allwefantasy/streamingpro.svg)](http://hits.dwyl.io/allwefantasy/streamingpro)

----------

##  WeChat Group

扫码添加小可爱微信号，添加成功后，发送  mlsql  这5个英文字母进群。

![](http://docs.mlsql.tech/upload_images/WX20200505-090326@2x.png)

