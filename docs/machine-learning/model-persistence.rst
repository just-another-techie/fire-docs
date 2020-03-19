Model Persistence
================

Save/ Load Model allows you to save your model to file and load it later in order to make predictions.

Fire Insights allows you to save the ML Model created. The ML Models can be loaded in the same or other workflows to be used for scoring. The ML Models can also be downloaded from HDFS Browse.

Spark ML Models
---------------

Spark ML models are saved into a directory with multiple files in it. Fire Insights has processors saving and loading the Spark ML models.

Save Model processor
+++++++++++++++++++++

.. figure:: ../_assets/model/savemodelconfigurations.PNG
   :alt: Modelsave
   :align: center
   :width: 60%
   
ML Save Workflow
+++++++++++++++++++++

.. figure:: ../_assets/model/mlmodelsave.png
   :alt: Modelsave
   :align: center
   :width: 60%
   
   
Load Model processor
+++++++++++++++++++++

.. figure:: ../_assets/model/loadmodelconfigurations.PNG
   :alt: Modelsave
   :align: center
   :width: 60%   
   
   
   
ML Load Workflow
+++++++++++++++++++++
   
.. figure:: ../_assets/model/mlmodelload.png
   :alt: Modelsave
   :align: center
   :width: 60%   

H2O Models
----------

H2O Models can be saved in binary format or in MOJO format. Fire Insights has processors for them.

Save H2o Model processor
+++++++++++++++++++++

.. figure:: ../_assets/model/h2omodelsaveconfigurations.PNG
   :alt: Modelsave
   :align: center
   :width: 60%
   
Load H2o Model processor
+++++++++++++++++++++
   
.. figure:: ../_assets/model/h2omodelloadconfiguration.PNG
   :alt: Modelsave
   :align: center
   :width: 60%

More details of saving and loading the H2O Models is available here:

http://docs.h2o.ai/h2o/latest-stable/h2o-docs/save-and-load-model.html



Save and Load H2O Workflow
++++++++++++++++++++++++++
   
.. figure:: ../_assets/model/h2osaveandload.png
   :alt: Modelsave
   :align: center
   :width: 60%
   
   
   
Scikit-Learn Models
--------------------

Scikit-Learn models are persisted with pickle. Fire Insights has processors for saving and loading the pickle files.

More details of the pickle format is available here:

https://scikit-learn.org/stable/modules/model_persistence.html


