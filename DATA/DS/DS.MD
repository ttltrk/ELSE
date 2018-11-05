
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [most used manuals](https://github.com/ttltrk/PRG/blob/master/MUM.MD)

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [ETL](https://github.com/ttltrk/ELSE/blob/master/DATA/DATA.MD) - [DataStage](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DSM.MD) - [DS own manuals](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DSOM.MD)

---

### DataStage 11.5

---

<h4 id='^'></h4>

1 - Introduction to DataStage

* <a href='#01'>IBM InfoSphere DataStage</a>
* <a href='#02'>Information Server</a>
* <a href='#03'>Information Server backbone</a>
* <a href='#04'>DataStage architecture</a>
* <a href='#05'>DataStage Administrator</a>
* <a href='#06'>DataStage Designer</a>
* <a href='#07'>DataStage Director</a>
* <a href='#08'>Developing in DataStage</a>
* <a href='#09'>DataStage project repository</a>
* <a href='#10'>Type of DataStage jobs</a>
* <a href='#11'>Design elements of parallel jobs</a>
* <a href='#12'>Pipeline parallelism</a>
* <a href='#13'>Patrition parallelism</a>
* <a href='#14'>Three-node partitioning</a>
* <a href='#15'>Configuration file</a>

---

2 - Deployment

* <a href='#16'>Information Server</a>
* <a href='#17'>Everything on one machine</a>
* <a href='#18'>DataStage on a separate machine</a>
* <a href='#'></a>
* <a href='#'></a>
* <a href='#'></a>
* <a href='#'></a>
* <a href='#'></a>
* <a href='#'></a>
* <a href='#'></a>

---

3 - Datastage Administration

---

4 - Work with metadata

---

5 - Create parallel jobs

---

6 - Access sequential data

---

7 - Partitioning and collecting algorithms

---

8 - Combine data

---

9 - Group processing stages

---

10 - Transformer stage

---

11 - Repository functions

---

12 - Work with relational data

---

13 - Job control

---

1 - Introduction to DataStage

<h4 id='01'>IBM InfoSphere DataStage</h4>

```
- Design jobs for Extraction, Transformation, and Loading (ETL)
- Ideal tool for data integration projects – such as, data warehouses, data marts, and system migrations
- Import, export, create, and manage metadata for use within jobs
- Build, run, and monitor jobs, all within DataStage
- Administer your DataStage development and execution environments
- Create batch (controlling) jobs
    - Called job sequence
```

<a href='#^'>^^^</a>

<h4 id='02'>Information Server</h4>

```
- Suite of applications, including DataStage, that share a common:
    - Repository
    - Set of application services and functionality
      - Provided by the Metadata Server component
        - By default an application named “server1”, hosted by an IBM WebSphere Application Server (WAS) instance
      - Provided services include:
        - Security
        - Repository
        - Logging and reporting
        - Metadata management
- Managed using the Information Server Web Console client
```

<a href='#^'>^^^</a>

<h4 id='03'>Information Server backbone</h4>

```
- Information Services Director
- Information Governance Catalog
- Information Analyzer
- FastTrack
- DataStage / QualityStage
- DataClick

- MetaData Server
    - Metadata Access Services
    - Metadata Analysis Services
    
- Information Server Web Console
- Repository

```

<a href='#^'>^^^</a>

<h4 id='04'>DataStage architecture</h4>

```
- DataStage clients
  - Administrator
  - Designer
  - Director
  
- DataStage engines
  - Parallel engine
    - Runs Parallel jobs
  - Server engine
    - Runs server jobs
    - Runs job sequences
```

```
Administrator - Configures DataStage projects and specifies DataStage user roles.
Designer - Creates DataStage jobs that are compiled into executable programs.
Director - Used to run and monitor the DataStage jobs, although this can also be done in Designer.
```

<a href='#^'>^^^</a>

<h4 id='05'>DataStage Administrator</h4>

```
Use the Administrator client to specify general server defaults, to add and delete
projects, and to set project defaults and properties.
```

<a href='#^'>^^^</a>

<h4 id='06'>DataStage Designer</h4>

```
DataStage Designer is where you build your ETL (Extraction, Transformation, Load)
jobs. You build a job by dragging stages from the Palette (lower left corner) to the
canvas. You draw links between the stages to specify the flow of data. In this example,
a Sequential File stage is used to read data from a sequential file. The data flows into a
Transformer stage where various transformations are performed. Then the data is
written out to target DB2 tables based on constraints defined in the Transformer and
SQL specified in the DB2 Connector stage.
```

<a href='#^'>^^^</a>

<h4 id='07'>DataStage Director</h4>

```
As your job runs, messages are written to the log. These messages display information
about errors and warnings, information about the environment in which the job is
running, statistics about the numbers of rows processed by various stages, and much
more.
```

<a href='#^'>^^^</a>

<h4 id='08'>Developing in DataStage</h4>

```
- Define global and project properties in Administrator
- Import metadata into the Repository
- Build job in designer
- Compile job in designer
- Run the job
```

<a href='#^'>^^^</a>

<h4 id='09'>DataStage project repository</h4>

```
All your work is stored in a DataStage project. Before you can do anything, other than
some general administration, you must open (attach to) a project.
```

<a href='#^'>^^^</a>

<h4 id='10'>Type of DataStage jobs</h4>

```
- Parallel jobs
  - executed by the DS parallel engine
  - compiled int OSH

- Server jobs
  - executed by the DS server engine
  - use a different set of stages than parallel jobs
  - runtime monitoring in the job log
  
- Job sequences
  - a server job that runs and controls jobs and other activities
  - can run both parallel jobs and other job sequences
```

<a href='#^'>^^^</a>

<h4 id='11'>Design elements of parallel jobs</h4>

```
- Stages

  - Passive stages (E and L of ETL)
    - Read data
    - Write data
    - Examples: Sequential file, DB2, Oracle, Peek stages

  - Processor (active) stages (T of ETL)
    - Transform data (transformer stage)
    - Filter data (transformer stage)
    - Aggregate data (Aggregator stage)
    - Generate data (Row Generator stage)
    - Merge data (Join, Lookup stages)
    
- Links
  - Pipes through which the data moves from stage-to-stage
```

<a href='#^'>^^^</a>

<h4 id='12'>Pipeline parallelism</h4>

```
- Transform, Enrich, Load stages execute in parallel
- Like a conveyor belt moving rows from stage to stage
  - Run downstream stages while upstream stages are running
- Advantages
  - Reduces disk usage for staging areas
  - Keeps processors busy
- Has limit on scalability
```

<a href='#^'>^^^</a>

<h4 id='13'>Partition parallelism</h4>

```
- Divide the incoming stream of data into subsets to be separately processed by an operation
- Each partition of data is processed by copies the same stage
- Facilitates near-linear scalability
```

```
Partitioning breaks a stream of data into smaller subsets. This is a key to scalability.
```

<a href='#^'>^^^</a>

<h4 id='14'>Three-node partitioning</h4>

```
Data -- subset1 -- Stage -- Node1
     -- subset2 -- Stage -- Node2
     -- subset3 -- Stage -- Node3
```

```
- here the data split into three partitions (nodes)
- the stage is executed on each partition of data separately and in parallel
- if the data is evenly distributed, the data will be processed three times faster
```

<a href='#^'>^^^</a>

<h4 id='15'>Configuration file</h4>

```
- Determines the degree of parallelism (numbers of partitions) of jobs that use it
- Every job runs under a configure file
- Each DS project has a default configuration file
  - Specified by the $APT_CONFIG_FILE job parameter
```

<a href='#^'>^^^</a>

---

2 - Deployment

<h4 id='16'>Information Server</h4>

```
An Information Server domain, consisting of the following:

  - Metadata Server Backbone, hosted by an IBM WebSphere Application Server (WAS) instance
  - One or more DS servers
    - Can be on the same system or on separate systems
  - One database manager instance containing the Repository database (XMETA)
  - Information Server clients
    - Web Console
    - DS clients
  - Additional Information Server products
    - Information Analyzer, Information Governance Catalog
    - QualityStage (part of DataStage), Data Click, FastTrack
```

<a href='#^'>^^^</a>

<h4 id='17'>Everything on one machine</h4>

```
- All information Server components on one system
  - DS server
  - Netadata Server backbone (WAS)
  - XMETA Repository 
  - Clients
- Additional client workstations can connect to this machine
```

<a href='#^'>^^^</a>

<h4 id='18'>DataStage on a separate machine</h4>

```
- IS components on multiple systems
  - DataStage servers
  - Metadata server WAS and XMETA repository
```

<a href='#^'>^^^</a>

<h4 id='19'>Metadata Server and DB2 on separate machines</h4>

```
- IS components all on separate systems
  - DS Server 
  - Metadata Server (WAS)
  - XMETA Repository
```

<a href='#^'>^^^</a>

<h4 id='20'>Information Server start-up</h4>

```
- Starting the Metadata Server (WAS) on Windows
- Starting the Metadata Server on Unix platforms
- By default, the startup services are configured to run automatically upon system startup
- To begin work in DS, double-click on a DS client icon, and then log in
- To begin work in the Information Server Web Console, open a web browser, enter the address of the services (WAS) system,
and then log in
```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

<h4 id=''></h4>

```

```

<a href='#^'>^^^</a>

---
