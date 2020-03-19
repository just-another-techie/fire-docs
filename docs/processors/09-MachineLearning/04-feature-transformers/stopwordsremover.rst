StopWordsRemover
=========== 

Filters out stop words from input. Null values from input array are preserved unless adding null to stopWords explicitly.

Output
--------------
It adds a new column containing the sequence of strings from the input column but with the stop words removed, to the incoming DataFrame.

Type
--------- 

ml-transformer

Class
--------- 

fire.nodes.ml.NodeStopWordsRemover

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - inputCol
        - Input Column
        - Column containing the array text from which the stop words have to be removed
      * - outputCol
        - Output Column
        - Contains array of text by dropping list of stop words
      * - caseSensitive
        - Case Sensitive
        - Case Sensitive
      * - stopWords
        - Comma Separated List of Custom Stop Words. If not provided, the default list of stop words would be used.
        - Custom List of Stop Words


Details
-------


Stop words filters out stop words from input. Null values from input array are preserved unless adding null to stopWords explicitly.

More at Spark MLlib/ML docs page : http://spark.apache.org/docs/latest/ml-features.html#stopwordsremover


