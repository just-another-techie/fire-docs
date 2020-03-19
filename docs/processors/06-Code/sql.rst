SQL
=========== 

This node runs the given SQL on the incoming DataFrame

Input
--------------
This type of node takes in a DataFrame and transforms it to another DataFrame

Output
--------------
This node runs the given SQL on the incoming DataFrame to generate the output DataFrame

Type
--------- 

transform

Class
--------- 

fire.nodes.etl.NodeSQL

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - tempTable
        - Temp Table
        - Temp Table Name to be used
      * - sql
        - SQL
        - SQL to be run
      * - schema
        - Schema
      * - outputColNames
        - Output Column Names
        - Name of the Output Columns
      * - outputColTypes
        - Output Column Types
        - Data Type of the Output Columns
      * - outputColFormats
        - Output Column Formats
        - Format of the Output Columns




