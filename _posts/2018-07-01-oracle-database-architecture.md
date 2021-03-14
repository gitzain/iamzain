---
layout: post
title: 
---
# Oracle Database Architecture

![https://iamzain.com/wp-content/uploads/2018/07/database-structure-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2018/07/database-structure-illustration-868x651.png)

As a designer we drop a blob onto a piece of graph paper and label it a database server. We never really fully understanding how it works and for the most part we never really need to. Will the article make you a database god? No. Will this article give you a good understanding of the different parts of an Oracle Database and what they do? Yes!

The thing we call an “Oracle Database” can be divided into two parts. The first is the database instance which lives in compute (processor) and memory (RAM). The second is actual database which lives in storage (disk) as files.

![http://iamzain.com/wp-content/uploads/2018/07/oracle-instance_vs_database.png](http://iamzain.com/wp-content/uploads/2018/07/oracle-instance_vs_database.png)

![http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5b39f2de2b6a28042227a159/1530524415676/oracle_instance_vs_database.gif](http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5b39f2de2b6a28042227a159/1530524415676/oracle_instance_vs_database.gif)

## **Oracle Database**

Let’s ignore the Oracle Instance for now and look at the Oracle Database. The Oracle Database is comprised of files.

### **Files**

These files provide permanent storage. The different types of Oracle Database files are listed below:

1. Data Files – The files the actual data is stored in.
2. Redo Log Files – As changes are made to the Data Files these changes are stored in the Redo Log Files. For example; an entry in the Redo Log File will specify what has changed and what it was before. The Redo Log Files are written to in a circular fashion – meaning when all the Redo Log Files are filled, the Redo Logs will then be started to be overwritten.
3. Archive Log Files – Optional files that are simply copies of Redo Log Files. Why have copies? Remember Redo Log files are overwritten once they are filled up. Once the Redo Logs are filed up they are then copied to a different location (by the Archiver process) and stored as Archive Log Files. The Redo Log Files can then be overwritten. Archive Log Files are used to recover the database.
4. Control Files – These files tell the Oracle Instance things like the name of the database, where the data files, redo files etc are.

## **Oracle Instance**

### **Memory**

The part of the Oracle Instance that sits in memory is called the System Global Area (SGA). The SGA has the following bits:

1. Buffer Cache – Changes are never directly writen to the Data Files. When manipulating data, that portion of the data (called Data Block) is copied into the Buffer Cache where it can then be accessed (read) or modified.
2. Shared Pool – This is quite a complicated structure and contains many bits. One of the main functions of this area is collecting, parsing, interpreting, and executing the SQL statements.
3. Redo Log Buffer – Whenever changes are made to data in the Buffer Cache data about the change is written to the Redo Log Buffer. Redo entries contain the information necessary to reconstruct, or redo, changes made to the database by INSERT, UPDATE, DELETE, CREATE, ALTER, or DROP operations. Redo entries are used for database recovery, if necessary.
4. Large Pool – An optional area of memory, used to relieve the burden place on the shared pool.
5. Java Pool – This is only required and used when the application using the database is going to use something called Java stored procedures.
6. Stream Pool – Reserved for something called Oracle Steam functions. We don’t need to know or care about these.

### **Processes**

The Oracle Instance has many processes. Background processes help keep the Oracle Instance and Database functioning smoothly. Five of the main background processes are listed below:

1. Database Writer (DBWn) – This process is in charge of actually writing changes from the Buffer Cache to the Data Files.
2. Log Writer (LGWR) – Writes the Redo Log Buffer to Redo Log Files on disk.
3. System Monitor (SMON) – Performs instance recovery, cleans up after dirty shutdowns
4. Process Monitor (PMON) – PMON is responsible for monitoring all Oracle processes. If any of the background processes fail, PMON will do process recovery.
5. Checkpoint (CKPT) – Regularly ensures any changes not yet wirtten to the Data Files are written then updates the Control Files to record it has just created a checkpoint.
6. Archiver – Copies the contents of a Redo Log File to another location, typically a disk file, when that log file becomes full.

## **Putting it all together 👏**

![http://iamzain.com/wp-content/uploads/2018/07/oracle_database_architecture.jpg](http://iamzain.com/wp-content/uploads/2018/07/oracle_database_architecture.jpg)

![http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5b3a01a78a922dbccfb9b1e6/1530528175695/Oracle+Database+Components.jpeg](http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5b3a01a78a922dbccfb9b1e6/1530528175695/Oracle+Database+Components.jpeg)