DecisionTreeRegression
=========== 

It supports both continuous and categorical features.

Input
--------------
This takes in a DataFrame and performs Decision Tree Regression

Output
--------------
The Decision Tree Regression Model generated is passed along to the next nodes. The input DataFrame is also passed along to the next nodes

Type
--------- 

ml-estimator

Class
--------- 

fire.nodes.ml.NodeDecisionTreeRegression

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - featuresCol
        - Features Column
        - Features column of type vectorUDT for model fitting
      * - labelCol
        - Label Column
        - The label column for model fitting
      * - predictionCol
        - Prediction Column
        - The prediction column created during model scoring.
      * - impurity
        - Impurity
        - The Criterion used for information gain calculation
      * - maxBins
        - Max Bins
        - The maximum number of bins used for discretizing continuous features.Must be >= 2 and >= number of categories in any categorical feature.
      * - maxDepth
        - Max Depth
        - The Maximum depth of a tree
      * - minInfoGain
        - Min Information Gain
        - The Minimum information gain for a split to be considered at a tree node
      * - minInstancesPerNode
        - Min Instances Per Node
        - The Minimum number of instances each child must have after split
      * - seed
        - Seed
        - The random seed
      * - cacheNodeIds
        - Cache Node Ids
        - The caching nodes IDs. Can speed up training of deeper trees.
      * - checkpointInterval
        - Checkpoint Interval
        - The checkpoint interval. E.g. 10 means that the cache will get checkpointed every 10 iterations.Set checkpoint interval (>= 1) or disable checkpoint (-1)
      * - maxMemoryInMB
        - Max memory
        - Maximum memory in MB allocated to histogram aggregation.
      * - gridSearch
        - Grid Search
      * - minInfoGainGrid
        - Min Information Gain Param Grid Search
        - Min Information Gain Parameters for Grid Search
      * - maxBinsGrid
        - Max Bins Param Grid Search
        - Max Bins Parameters for Grid Search
      * - maxDepthGrid
        - Max Depth Param Grid Search
        - Max Depth Parameters for Grid Search


Details
-------


Decision tree supports both continuous and categorical features.

More at Spark MLlib/ML docs page : https://spark.apache.org/docs/1.6.0/ml-classification-regression.html#decision-tree-regression


