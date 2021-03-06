
## KAP 概览

Kyligence Analytics Platform（KAP）大数据智能分析平台是基于*Apache Kylin*的，在超大数据集上提供亚秒级分析能力的企业级产品，为业务用户、分析师及工程师提供简单、快捷的大数据分析服务。在继承Apache Kylin的高性能查询，易用建模，多协议支持，非侵入式架构等突出优点的同时，KAP在企业用户所关注的实施效率、安全可控、性能优化、自助式敏捷BI、系统监控等方面进行了全方位的创新。

**KyStorage 列式存储引擎**

*KyStorage*是Kyligence研发的基于HDFS的列式存储引擎，支持多路复合索引，针对超高基数维度、复杂过滤条件等的场景进行了专门优化，相对*Apache Kylin*，查询性能有几倍到几十倍的提升，在存储空间上也有超过50％的节省。

**明细数据查询**

基于*KyStorage*列式存储引擎，及倒排索引等多种索引技术，突破了传统OLAP引擎仅能查询聚合数据的局限，全面地支持了明细数据的查询，优化了对宽表的支持，降低了数据建模的难度，更好地服务数据探索式分析场景。

**KyAnalyzer 敏捷BI自助多维分析工具**

内置敏捷BI平台*KyAnalyzer*，用户仅需浏览器，以熟悉的可拖拽方式交互地探复杂数据源，支持钻取，上卷，切片，切块，旋转等多维分析方法，支持数十种可视化报表技术，简易地多格式数据分享，极大地提高了业务人员分析大数据的效率。

**更多企业级功能**

支持开箱即用的用户管理及单元格级别的访问控制方式，可与用户已有访问认证体系深度集成，保证数据访问的可管理性、可追溯性。

支持Percentitle等分析函数

**兼容主流Hadoop发行版**

KAP兼容开源Hadoop及主流商业Hadoop发行版，可运行在*Apache Hadoop*，*Hortonworks HDP*，*Microsoft HDInsight*，*AWS EMR*等发行版和平台，并与*Cloudera CDH* 实现了产品相互认证。



![](images/kap_eco.jpeg)



### KAP与Apache Kylin比较

|                  | Apache Kylin   | KAP企业版                      | KAP高级企业版                    |
| ---------------- | -------------- | --------------------------- | --------------------------- |
| **定位**           | OLAP on Hadoop | Data Warehouse on Hadoop    | Data Warehouse on Hadoop    |
| **核心**           | Apache Kylin   | Apache Kylin                | Apache Kylin                |
| **查询性能**         | 亚秒级查询延迟        | 与Apache Kylin一致             | **比Apache Kylin快3～40倍**     |
| **并行计算**         | Coprocessor    | Coprocessor                 | **Spark**                   |
| **存储引擎**         | HBase          | HBase                       | **自主研发列式存储引擎KyStorage**     |
| **索引**           | 单索引            | 单索引                         | **多路复合索引**                  |
| **超高基维度支持**      | 有限             | 有限                          | **高效地支持**                   |
| **超宽表支持**        | 有限             | 有限                          | **高效地支持**                   |
| **明细数据查询**       | 有限             | 有限                          | **高效地支持**                   |
| **安全机制**         | 有限             | **LDAP/Kerberos/单元格级别访问控制** | **LDAP/Kerberos/单元格级别访问控制** |
| **敏捷BI工具**       | 无内置            | **内置敏捷BI工具KyAnalyzer**      | **内置敏捷BI工具KyAnalyzer**      |
| **技术支持**         | 开源社区邮件组，没有SLA  | 支持SLA的5*8或7*24              | 支持SLA的5*8或7*24              |
| **KyBot自助式服务平台** | 不包含，需要单独购买     | 包含                          | 包含                          |

