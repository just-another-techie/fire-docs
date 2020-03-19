Data Sources
------------

How does one define a new data source and establish a connection?
=============
 
Fire platform has various OOTB connectors to HIVE, Flume, Kafka, HBase, Solr.
For all other structured or unstructured datasets on HDFS or CloudBricks, Fire platform can identify the schema on the fly when a new dataset is created in Fire pointing to a data source. The schema can be updated right there as well.
Fire workflow execution writes a summary of its output to MySQL/Oracle/H2 which is accessible by the users of the system.

