# Advanced Cloud Hadoop / Spark Setup

## Development Environment Setup Information

You have a number of options - although it is possible for you to set up a local Hadoop/Spark cluster, I do NOT recommended this approach as it's needlessly complex for initial study.  Rather I do recommend that you use a partially or fully-managed cluster.  For learning, I most often use a **fully-managed (free tier) cluster**.  Also, I usually use a single-node cluster to start.

### 1. SaaS - Databricks --> MANAGED

Databricks offers managed Apache Spark clusters.  Databricks can run on AWS, Azure or GCP --> announced in 2021 - [link](https://cloud.google.com/databricks).
In my 'Scaling Cloud Spark' course, I use Databricks running on AWS, as the community editor is simple and fast to set up for learning purposes.

<img src="https://github.com/lynnlangit/learning-hadoop-and-spark/blob/master/images/word-count-databricks.png" width=600>
    
- Use **Databricks Community Edition** (managed, hosted Apache Spark), run on AWS.  Example notebook shown in screenshot above.
    - uses Databricks (Jupyter-style) notebooks to connect to a one or more custom-sized and managed Spark clusters
    - creates and manages your data files stored in cloud buckets as part of Databricks service 
    - uses DFS file system in cluster data operations
    - use **Databricks AWS community** edition (simplest set up - free tier on AWS) - [link](https://databricks.com/try-databricks) --OR--
    - use **Databricks Azure trial** edition - Azure may require a pay-as-you-go account to get needed CPU/GPU resources
    - try **Databricks on GCP beta** - announced recently - [link](https://cloud.google.com/databricks)
    
---

### 2. PaaS Cloud on GCP (or AWS) --> PARTIALLY-MANAGED

<img src="https://github.com/lynnlangit/learning-hadoop-and-spark/blob/master/images/emr-studio.png" width=600>

- Setup a Hadoop/Spark managed cloud-cluster via **GCP Dataproc or AWS EMR**
    - see `setup-hadoop` folder in this Repo for instructions/scripts
        - create a GCS (or AWS) **bucket** for input/output job data
        - see `example_datasets` folder in this Repo for sample data files
    - for **GCP use DataProc** includes Jupyter notebook interface --OR--
    - for **AWS use EMR** you can use EMR Studio (which includes managed Jupyter instances) - [link](https://aws.amazon.com/blogs/big-data/amazon-emr-studio-preview-a-new-notebook-first-ide-experience-with-amazon-emr/) example screenshot shown above
    - for Azure it is possible to use their HDInsight service.  I prefer Databricks on Azure because I find it to be more feature complete and performant. 
    

---

### 3. IaaS local or cloud --> MANUAL
    
- Setup Hadoop/Spark locally or on a 'raw' cloud VM, such as **AWS EC2**
    - NOT RECOMMENDED for learning - too complex to set up
- Cloudera Learning VM - also NOT recommended, changes too often, documentation not aligned
    - link to Cloudera downloads - [link](https://www.cloudera.com/downloads.html)

---
 
## Example Jobs or Scripts

**EXAMPLES** from `org.apache.hadoop_or_spark.examples` - link for [Spark examples](https://github.com/apache/spark/tree/master/examples/src/main/scala/org/apache/spark/examples)

- Run a Hadoop **WordCount** Job with Java (jar file)
- Run a Hadoop and/or Spark **CalculatePi** (digits) Script with PySpark or other libraries
- Run using Cloudera shared demo env 
    - at `https://demo.gethue.com/` 
    - login is user:`demo`, pwd:`demo`
---

## Other LinkedIn Learning Courses on Hadoop or Spark

There are ~ 10 courses on Hadoop/Spark topics on LinkedIn Learning.  See graphic below  
![Learning Paths](https://github.com/lynnlangit/learning-hadoop-and-spark/blob/master/images/path.png)

- **Hadoop** for Data Science Tips and Tricks - [link](https://www.linkedin.com/learning/hadoop-for-data-science-tips-tricks-techniques)
    - Set up Cloudera Enviroment
    - Working with Files in HDFS
    - Connecting to Hadoop Hive
    - Complex Data Structures in Hive
- **Spark** courses - [link](https://www.linkedin.com/learning/search?entityType=COURSE&keywords=Spark&software=Apache%20Spark~Hadoop)
    - Various Topics - see screenshot below

![LinkedInLearningSpark](https://github.com/lynnlangit/learning-hadoop-and-spark/blob/master/images/spark-courses.png)
