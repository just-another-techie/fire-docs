MultiCastColumnType
=========== 

This node creates a new DataFrame by casting input columns with a new data type

Input
--------------
This type of node takes in a DataFrame and transforms it to another DataFrame

Output
--------------
This node casts the data type of columns as specified

Type
--------- 

transform

Class
--------- 

fire.nodes.etl.NodeMultiCastColumnType

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - inputColNames
        - Columns
        - Columns
      * - outputColTypes
        - New Data Type
        - New data type(INTEGER, DOUBLE, STRING, LONG, SHORT)
      * - replaceExistingCols
        - Replace Existing Cols
        - Whether to replace existing Columns or create New Ones




