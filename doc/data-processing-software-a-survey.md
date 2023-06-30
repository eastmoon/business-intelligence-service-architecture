# 數據處理軟體調研 ( Data Processing software a survey )

#### Source Layer

+ Stream
    - [Kafka](https://zh.wikipedia.org/zh-tw/Kafka)
        + [Nifi](https://nifi.apache.org/)
        + [StreamSet](https://docs.streamsets.com/portal/platform-transformer/latest/transformer/GettingStarted/GettingStarted-Title.html#concept_a1b_zf4_pgb)
            - [Announcing StreamSets Data Collector 3.11.0 and StreamSets Data Collector Edge 3.11.0](https://streamsets.com/blog/announcing-streamsets-data-collector-3-11-0-and-streamsets-data-collector-edge-3-11-0/)
        + [Flume](https://flume.apache.org/)
+ Object Storage
    - [MinIO](https://min.io/)
        - [Apache Ozone](https://ozone.apache.org/)
            + [Breaking the HDFS Speed Barrier - a First for Object Storage](https://blog.min.io/hdfsbenchmark/)
            + [How is Apache Minio different than Apache Hadoop?](https://www.quora.com/How-is-Apache-Minio-different-than-Apache-Hadoop)
            + [Hadoop vs Minio - stackshare](https://stackshare.io/stackups/hadoop-vs-minio)
        - [Upload Files Using Pre-signed URLs](https://min.io/docs/minio/linux/integrations/presigned-put-upload-via-browser.html)
        - [Posting a File with Curl](https://reqbin.com/req/c-dot4w5a2/curl-post-file)
    - [Ceph](https://docs.ceph.com/en/quincy/)
    - [OpenIO](https://docs.openio.io/latest/source/sandbox-guide/quickstart.html)
+ 網頁匯入資料，整合 HFS 呈現內容
+ 網頁匯入 SSL 註冊，Rsync、SCP 匯入資料，整合 HFS 呈現內容
    - 以網頁上傳 SSH KEY，並取得匯入的用戶名稱
    - 匯入用戶名稱僅能存在一定時間
    - 匯入用戶僅能對特定目錄上傳內容
    - 上傳內容最終匯入到指定目錄

#### Model Layer

+ NumPy
+ PyTorch
+ OpenCV
+ OpenVINO
+ Scikit-Learn
+ Tensorflow

#### Application

+ [Grafana](https://grafana.com/)
+ [Http File Server](https://github.com/eastmoon/infra-hfs)

#### Framework

+ [Gitlab](https://github.com/eastmoon/infra-gitlab)
+ [Jenkins](https://github.com/eastmoon/infra-jenkins)
    - [How to Configure Jenkins Master Slave Setup.](https://digitalvarys.com/how-to-configure-jenkins-master-slave-setup/)
+ [HOP](https://hop.apache.org/)
    - [Kettle](https://github.com/pentaho/pentaho-kettle)
    - [7 key points to successfully upgrade from Pentaho to Apache Hop](https://www.know-bi.be/blog/upgrade-to-apache-hop)
+ [Airflow](https://github.com/eastmoon/infra-airflow)
+ [Flink](https://github.com/eastmoon/infra-flink)
+ [Spark](https://github.com/eastmoon/infra-spark)
+ [Hadoop](https://zh.wikipedia.org/zh-tw/Apache_Hadoop)
    - [Hadoop Architecture](https://hackr.io/blog/hadoop-architecture)
    - [Setting Up ETL in Hadoop: 5 Easy Steps](https://hevodata.com/learn/etl-in-hadoop/)
    - [Tutorial 2: Introduction to Hadoop Architecture, and Components](https://www.softwaretestingclass.com/introduction-to-hadoop-architecture-and-components/)

#### Database

+ OLTP
	- [PostgreSQL](https://zh.wikipedia.org/zh-tw/PostgreSQL)
+ OLAP
  - [Greenplum](https://greenplum.org/)
	- [Cassandra](https://zh.wikipedia.org/zh-tw/Cassandra)
+ Converged database
	- [MySQL](https://www.mysql.com/)
	- [Oracle](https://zh.wikipedia.org/wiki/%E7%94%B2%E9%AA%A8%E6%96%87%E5%85%AC%E5%8F%B8)
	- [MariaDB](https://zh.wikipedia.org/zh-tw/MariaDB)
+ Cache ( Semi-structured data )
	- [MongoDB](https://zh.wikipedia.org/zh-tw/MongoDB)
	- [Elasticsearch](https://github.com/eastmoon/infra-elk)
+ [Productionizing Machine Learning with Delta Lake](https://www.databricks.com/blog/2019/08/14/productionizing-machine-learning-with-delta-lake.html)

## 文獻

+ Image processing
    - [Image processing wiki](https://zh.wikipedia.org/wiki/%E5%9B%BE%E5%83%8F%E5%A4%84%E7%90%86)
    - [IPOL Journal · Image Processing On Line](http://www.ipol.im/)
    - [Image processing online tutorials](http://www.imageprocessingplace.com/root_files_V3/tutorials.htm)
    - [Digital Image procesing](https://www.youtube.com/playlist?list=PLZ9qNFMHZ-A79y1StvUUqgyL-O0fZh2rs)
    - [Image Processing online demo](http://felixniklas.com/imageprocessing/)
    - [Basic Image Processing Demos](http://robotics.eecs.berkeley.edu/~sastry/ee20/)

+ Computer vision
    - [Machine learning coursera](https://www.youtube.com/watch?v=qeHZOdmJvFU&list=PLZ9qNFMHZ-A4rycgrgOYma6zxF4BZGGPW)
    - [What is an Image Processing Framework for Machine Learning?](https://www.iguazio.com/glossary/image-processing-framework/)

+ Machine learning
    - [Top 15 Machine Learning Frameworks for Machine Learning Experts](https://intellipaat.com/blog/machine-learning-frameworks/)

+ ETL
    - [TOP 5 ENTERPRISE ETL TOOLS. HOW TO CHOOSE THE BEST?](https://freshcodeit.com/freshcode-post/top-5-enterprise-etl-tools)

+ Object Storage
    - [4 Open Source Object Storage Platforms for 2023](https://betterprogramming.pub/4-open-source-object-storage-platforms-for-2021-ceeaceb7e273)
    - [架構師都知道的分布式對象存儲解決方案](https://kknews.cc/zh-tw/code/vrlljky.html)

+ Database
    - [什麼是 OLTP？什麼是 OLAP？](https://datadrivenai.wordpress.com/2019/11/01/%E4%BB%80%E9%BA%BC%E6%98%AF-oltp%EF%BC%9F%E4%BB%80%E9%BA%BC%E6%98%AF-olap%EF%BC%9F/)
    - [OLTP vs OLAP: Comparison between OLAP and OLTP](https://mindmajix.com/oltp-vs-olap)
    - [Top 10 Databases to Use in 2021](https://towardsdatascience.com/top-10-databases-to-use-in-2021-d7e6a85402ba)
    - [Greenplum 和 PostgreSQL 的關係為何？](https://www.omniwaresoft.com.tw/product-news/greenplum-news/differences-between-greenplum-and-postgresql/)
