HDFS REST API
=============

Overview
--------

The HDFS REST API's, allow you to interact with the HDFS of the Hadoop Cluster Fire is connected to.

Below are the various HDFS API's available in Fire

They should be executed after you have logged into Fire

Get List of Files in Directory
----------------

Returns list of all the files on hdfs in the users home directory
::

  curl -X GET --header 'Accept: application/json' 'http://localhost:8080/api/v1/hdfs'
  
Create HDFS directory
---------------------

::

   curl -X POST --header 'Content-Type: application/json' --header 'Accept: text/plain' 'http://localhost:8080/api/v1/hdfs/dir/create'

Get list of files in HDFS in the specified directory
--------------------------------------------------------
 
Returns list of files in HDFS in the specified directory(/user/sparkflows/)

::

   curl -X GET --header 'Accept: application/json' 'http://localhost:8080/api/v1/hdfs/dir/open?path=%2Fuser%2Fsparkflows%2F'
   
Get list of all the files on hdfs in the users home directory in sorted order
----------------------------------------------------------------------------------

*sortPara: alphabetical

*path: /user/sparkflows/

::
   
   curl -X GET --header 'Accept: application/json' 'http://localhost:8080/api/v1/hdfs/files?sortPara=alphbetical&path=%2Fuser%2Fsparkflows%2F'
   
  

Upload file
-----------

::

   curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' 'http://localhost:8080/api/v1/hdfs/files/upload' -b /tmp/cookies.txt
  

Deletes a file from HDFS
------------------------
*path: /user/sparkflows/Airline.csv

::

  curl -X DELETE --header 'Accept: text/plain' 'http://localhost:8080/api/v1/hdfs/files/delete?path=%2Fuser%2Fsparkflows%2FAirline.csv'
   
Download HDFS file
------------------

*path: /user/sparkflows/Airline.csv

::

  curl -X GET --header 'Accept: application/json' 'localhost:8080/api/v1/hdfs/files/download?path=%2Fuser%2Fsparkflows%2FAirline.csv'

Rename HDFS File
----------------

*sourceFilePath: /user/sparkflows/Airline.csv

*destinationFilePath: /user/sparkflows/airline.csv

::
   
  curl -X GET --header 'Accept: text/plain' 'http://localhost:8080/api/v1/hdfs/files/rename?sourceFilePath=%2Fuser%2Fsparkflows%2FAirline.csv&destinationFilePath=%2Fuser%2Fsparkflows%2Fairline.csv'
 
Get  first X bytes of content of a file
----------------------------------------------------------

*path: /user/sparkflows/Airline.csv

::

  curl -X GET --header 'Accept: text/plain' 'http://localhost:8080/api/v1/hdfs/files/open?path=%2Fuser%2Fsparkflows%2FAirline.csv'
  
  
