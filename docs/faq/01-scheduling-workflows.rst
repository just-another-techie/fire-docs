Scheduling Workflows
--------------------

How can I schedule the workflows I create ?
===========

Fire Insights saves workflow definitions as JSON files. These workflows are executed through spark-submit.

Fire Insights has a scheduler which allows Workflows to be scheduled at regular intervals.

Since the workflows are submitted with spark-submit, they can also be easily scheduled with Oozie, crontab etc.
