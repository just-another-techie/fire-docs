Executing Workflows
===================

Fire Workflows can be executed in the following ways:
 
 * **Interactively within the User Interface**
 * **Submitting the workflows using spark-submit through the command line**
 * **Scheduling for execution with your scheduler of choice**
 
Interactively within the User Interface
------------------------------------------

Workflows can be executed from the browser by going into the Execute page of the workflow.


.. figure:: ../../_assets/user-guide/workflow/4.PNG
   :alt: Workflow
   :align: center
   :width: 60%

Executing Workflows with spark-submit
--------------------------------------
 
Workflows are saved as text files in JSON format.
Workflows can be submitted to be run on the cluster with spark-submit::
  
    spark-submit    --class    fire.execute.WorkflowExecuteFromFile    --master yarn    --deploy-mode client    --executor-memory 1G    --num-executors 1    --executor-cores 1       fire-core-1.4.2-jar-with-dependencies.jar       --postback-url http://<machine>:8080/messageFromSparkJob        --job-id 1         --workflow-file      kmeans.wf


In the above:

+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameter          | Details                                                                                                                                                                                                |
+====================+========================================================================================================================================================================================================+
| fire-core jar file | It is the fire-core jar file required code for executing the workflow. The fire-core jar file is in the fire-lib directory of the Fire install                                                   |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| postback-url       | http://<machine>:8080/messageFromSparkJob is the postback URL for fire UI. <machine> should be the machine name on which Fire is running. 8080 should be the port on which Fire is running |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| job-id             | 1 is the job id. It can be of any value for now                                                                                                                                                           |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| workflow-file      | kmeans.wf is the json workflow file containing the kmeans workflow in this case.                                                                                                                       |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


 For providing extra variables to the workflow, the following parameters can be added to spark-submit::
 
    --var name1=value1   --var name2=value2    --var name3=value3
 
In the workflow, these variables can be used with $name1    $name2
Specific nodes make use of the variables by substituting $name with the value provided for the name.
 
For running the workflow in debug mode, add the following parameters::

    --debug true
    

Workflow JSON
--------------
 
In Fire, workflows are saved as JSON Strings. 
  
The View JSON Workflow page of the Workflow displays the JSON representations of the workflow. 



.. figure:: ../../_assets/user-guide/json-workflow.png
   :alt: Sparkflows Json Workflow
   :align: center
 
 
Scheduling Workflow execution with Scheduler of choice
----------------------------------------------------------
 
Since Fire workflows can be submitted with spark-submit, you can use your scheduler of choice for scheduling the execution of the workflows.
 
- Click on Schedule Button of Workflow we want to schedule

.. figure:: ../../_assets/user-guide/workflow/5.PNG
   :alt: Workflow
   :align: center
   :width: 60%  
 
 
- Click on Tab Schedule New Job for Workflow
 
 .. figure:: ../../_assets/user-guide/workflow/6.PNG
   :alt: Workflow
   :align: center
   :width: 60% 
 
 - Update the scheduled timing & email notifications after success & failure of workflow as per our requirments.
 
.. figure:: ../../_assets/user-guide/workflow/7.PNG
   :alt: Workflow
   :align: center
   :width: 60%    

- Click on OK to save the changes.

.. figure:: ../../_assets/user-guide/workflow/8.PNG
   :alt: Workflow
   :align: center
   :width: 60%  

 
Debugging Workflows
-------------------
 
Many times it is helpful to be able to debug the workflows. One easy way is to check the debug checkbox in the UI when executing the workflow.
 
Running in debug mode does a few things:

* Performs a count() after executing each Processor. This makes it easier to track errors. It takes out Fire lazy execution from the picture.
* Displays the number of records processed at each stage.
* Display more information, for each SQL etc. which are being executed.





