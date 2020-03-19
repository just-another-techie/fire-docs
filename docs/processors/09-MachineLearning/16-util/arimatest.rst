ARIMATEST
=========== 

Fits the ARIMA model and tests for accuracy. It splits the data for training and test, fits the ARIMA model on the training set and then finds the accuracy on the test set.

Type
--------- 

transform

Class
--------- 

fire.nodes.ml.NodeARIMATest

Fields
--------- 

.. list-table::
      :widths: 10 5 10
      :header-rows: 1

      * - Name
        - Title
        - Description
      * - inputCol
        - Input Series Column
        - Input Series Column Name
      * - split
        - Training Split Size
        - Split size for training and test. 0.5 splits it to 50% for training and 50% for test
      * - autofit
        - AutoFit
        - Should it automatically find the p, d, q values for the best model, or take the user supplied values
      * - p
        - P
        - 
      * - d
        - D
        - 
      * - q
        - Q
        - 




