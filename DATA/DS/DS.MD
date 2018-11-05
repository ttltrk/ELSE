
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [most used manuals](https://github.com/ttltrk/PRG/blob/master/MUM.MD)

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [ETL](https://github.com/ttltrk/ELSE/blob/master/DATA/DATA.MD) - [DataStage](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DSM.MD) - [DS own manuals](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DSOM.MD)

---

### DataStage 11.5

---

<h4 id='^'></h4>

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

---

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

---

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

---

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

---

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

---

<h4 id='05'>DataStage Administrator</h4>

```
Use the Administrator client to specify general server defaults, to add and delete
projects, and to set project defaults and properties.
```

<a href='#^'>^^^</a>

---

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

---

<h4 id='07'>DataStage Director</h4>

```
As your job runs, messages are written to the log. These messages display information
about errors and warnings, information about the environment in which the job is
running, statistics about the numbers of rows processed by various stages, and much
more.
```

<a href='#^'>^^^</a>

---

<h4 id='08'>Developing in DataStage</h4>

```
- Define global and project properties in Administrator
- Import metadata into the Repository
- Build job in designer
- Compile job in designer
- Run the job
```

<a href='#^'>^^^</a>

---

<h4 id='09'>DataStage project repository</h4>

```
All your work is stored in a DataStage project. Before you can do anything, other than
some general administration, you must open (attach to) a project.
```

<a href='#^'>^^^</a>

---

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

---

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

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---

<h4 id=''></h4>

<a href='#^'>^^^</a>

---
