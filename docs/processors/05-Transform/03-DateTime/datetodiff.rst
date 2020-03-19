DateDifference
=========== 

This node finds difference between two dates

Input
--------------
It accepts a DataFrame as input from the previous Node

Type
--------- 

transform

Class
--------- 

fire.nodes.etl.NodeDateDiff

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - fromDate
        - FromDate
        - From date column name
      * - toDate
        - Todate
        - To date column name
      * - useCurrentDateAsToDateCol
        - useCurrentDateAsToCol
        - Current Date As ToDate
      * - days
        - Days
        - Days difference
      * - hours
        - Hours
        - Hours difference
      * - minutes
        - Minutes
        - Minutes difference
      * - seconds
        - Seconds
        - Seconds difference


Details
-------


Calculates difference between 2 given dates.
Difference between dates is displayed in days, hours, minutes, and seconds columns.


Examples
-------

Format Examples
+++++++++++++++
dd-MM-yy : 30-11-95 to 19-02-18 diff- 8608 days : 206609 hours : 12396574 min :	743794461 : second
dd-MM-yyyy : 10-02-1996 to 20-09-2017 diff- 8536 days : 204881 hours : 12292884 min :	737573070 : second
MM-dd-yyyy : 19-10-1994 to 06-12-2017 diff- 9015 days : 216377 hours : 12982644 min :	778958670 : second
yyyy-MM-dd : 1994-12-25 to 2019-01-16 diff- 8948 days : 214769 hours : 12886164 min :	773169870 : second
yyyy-MM-dd HH:mm:ss : 2012-01-31 23:59:59 to 2010-12-30 22:59:59 diff-397 days: 1 hour: 0 minutes : 0 seconds



Input
----------

.. list-table:: 
   :widths: 10 50 50
   :header-rows: 2

   * - id
     - date_string
     - date_string1
   
   * - IntegerType
     - TimestampType
     - StringType
     
   * - 0
     - 2011-1-1 00:00:00.0
     - 05/26/2016 01:01:01
   
   * - 1
     - 2012-1-14 01:00:00.0
     - 06/22/2017 01:00:00
   
   * - 2
     - 2013-12-10 02:00:00.0
     - 01/12/2016 01:01:01
     

Parameters
------------

.. list-table:: 
   :widths: 40 10
   :header-rows: 1
   
   * - Name
     - Value
     
   * - FromDate
     - date_string
     
   * - Todate
     - 
     
   * - useCurrentDateAsToCol
     - true
     
   * - Days
     - true
     
   * - Hours
     - true
     
   * - Minutes
     - true
     
   * - Seconds
     - true  
 
Output
--------------

.. list-table:: 
   :widths: 10 50 50 30 30 30 30
   :header-rows: 1

   * - id
     - date_string
     - date_string1
     - DateDiff
     - HoursDiff
     - MinutesDiff
     - SecondsDiff
   
   * - 0
     - 2011-1-1 00:00:00.0
     - 05/26/2016 01:01:01
     - 3192
     - 76615
     - 4596911
     - 275814696
   
   * - 1
     - 2012-1-14 01:00:00.0
     - 06/22/2017 01:00:00
     - 2814
     - 67542
     - 4052531
     - 243151896
   
   * - 2
     - 2013-12-10 02:00:00.0
     - 01/12/2016 01:01:01
     - 2118
     - 50837
     - 3050231
     - 183013896
