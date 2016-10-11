> KyAnalyzer is developed by Kyligence based on Saiku. KyAnalyzer automatize some unecessary operations to make user analyze data easier and quicker.
>
> This document is based on KyAnalyzer version 0.2.

###Pre-Condition
* KAP should be version 2.1 or later
* Apache Kylin version should be 1.5.4.1 or later.
* KyAnalyzer does not supprt *left join*,you should use *inner join* when create cube mode in KAP.

### Install
Get the package KyAnalyzer-{version}.zip from Kyligence Inc, and download the customized mondrian mondrian-kylin-{version}.jar from GitHub kylin-mondrian repository: (https://github.com/Kyligence/kylin-mondrian/blob/master/build/), if the version is updated, please use the latest jar.
Unzip KyAnalyzer package, copy mondrian-kylin-{version}.jar into saiku-server/tomcat/webapps/saiku/WEB-INF/lib.
Edit kyanalyzer-beans.properties in WEB-INF, update KAP host and port to KAP server. The key *kap.host* is the IP address of KAP, and key *kap.port* is the port of KAP REST API, default port is 7070.

Run start-saiku.sh under saiku-server to start KyAnalyzer, the default port is 8080. When the server is started, please visit http://{hostname}:8080. If you want to stop the server, please run stop-saiku.sh.

 If the server is not started normally, please check the logs under tomcat/logs for details.


#### Files under home directory

![](/images/integration/kyanalyzer/server_dir.png)


KyAnalyzer will save data under the directory *repository* and *data*, when you upgrade  KyAnalyzer, need to backup these two directories.

### Authentication
KyAnalyzer authenticates user at KAP side, so you can use KAP user and password to login. Users with *Admin* Role in KAP are also *Admin* in KyAnalyzer.
![](/images/integration/kyanalyzer/analyzer_login.png)

### Admin Page
Only the admin could visit this page.
To import the Cube from KAP, Saiku needs to create schema and datasource for each cube in KAP by default. KyAnalyzer automatize the flow, user don't have to write schema by themeselves.
Click **Sync Cubes From Kylin** on the left side, the right panel will list all projects from KAP.

![](/images/integration/kyanalyzer/admin_sync.png)

Click the green button **Sync Cubes From Kylin** after select project, KyAnalyzer will create *schema* and *datasource* for all cubes under this project whose status is 'READY'.

![](/images/integration/kyanalyzer/sync_done_tip.png)

The schema could be edited online in KyAnalyzer, it's not necessary at most time.

### New Query
Click *New Query* button at navigation bar, then click *Refresh* button to fetch the latest data, select the cube under *Cubes* menu, now all dimensions and measures are shown.

![](/images/integration/kyanalyzer/cube_refresh.png)

KyAnalyzer supports many types of visulization, table, bar, stacked bar, line chart, area chart, heat grid, tree map, pie chart, dot chart, water fall chart ,etc.

#### Bar
![](/images/integration/kyanalyzer/bar_chart.png)

#### Pie
![](/images/integration/kyanalyzer/pie_chart.png)

#### Pivotal Table
![](/images/integration/kyanalyzer/pivotal_table.png)

#### COUNT DISTINCT
![](/images/integration/kyanalyzer/count_distinct.png)

#### Hierarchy Data
![](/images/integration/kyanalyzer/hierarchy_table.png)


### Result Filter
To filter the results, you can click the dimension name and see the filter dialog, input the search pattern to filter the select options, and select your options, you can include or exclude the options.

![](/images/integration/kyanalyzer/filter.png)

### Save Query Result
You can export results to files(csv, pdf, excel) or pictures.

#### Export grid to files
![](/images/integration/kyanalyzer/export_table.png)

#### Export chart to picture
![](/images/integration/kyanalyzer/export_image.png)

### Save query results in KyAnalyzer
The query result could be saved in KyAnalyzer, so next time when you login, you don't have to select your dimensions and measures again.

#### Save Query
![](/images/integration/kyanalyzer/save_query.png)

#### Open Query
![](/images/integration/kyanalyzer/open_query.png)

#### Execute Query
![](/images/integration/kyanalyzer/execute_query.png)





