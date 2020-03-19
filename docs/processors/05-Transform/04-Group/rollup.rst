Rollup
=========== 

Rollup Node generates a result set that shows aggregates for a hierarchy of values in the selected columns.

Type
--------- 

transform

Class
--------- 

fire.nodes.etl.NodeRollup

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - rollupCols
        - Rollup Columns
        - 
      * - aggregateCols
        - Aggregate Columns
        - Aggregate Columns
      * - aggregateOperations
        - Aggregate Operation to use
        - Aggregate Operation


Examples
----------

Input
------

.. list-table:: 
   :widths: 20 20 20
   :header-rows: 1

   * - name
     - age
     - height
     
   * - Alice
     - 5
     - 80
     
   * - Alice
     - 5
     - 80
     
   * - Alice
     - 10
     - 80
     
   * - James
     - 5
     - 50
     
   * - James
     - 10
     - 60
    
   * - James
     - 7
     - 80
     
 
Parameters
-------------

.. list-table:: 
   :widths: 10 25
   :header-rows: 1

   * - Name
     - Value
   
   * - Rollup Columns
     - name

.. list-table:: 
   :widths: 10 25 40
   :header-rows: 1
   
   * - Id
     - Aggregate Columns
     - Aggregate Operation to Use
   
   * - 1
     - age
     - max
   
   * - 2
     - height
     - min
   

Output
---------

.. list-table:: 
   :widths: 20 20 20
   :header-rows: 1

   * - name
     - max_age
     - min_height
     
   * - Alice
     - 10
     - 80
     
   * -
     - 10
     - 50
     
   * - James
     - 10
     - 50


