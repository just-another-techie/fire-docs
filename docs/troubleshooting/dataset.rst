Dataset
=======


I am getting an error when clicking 'Update' button on the Create/Update Dataset page
--------------------------------------------------------------------------------------

You may see the error below::

  Unable to retrieve schema for this path :: Bad header for field, should start with a character or _ and can contain only alphanumerics and _ 0:" id 1 "


* This is because one of the column names of the header is not in the right format. In this case the column name ``id 1`` contains a space.

* Only ``alphanumerics and _`` are permitted in the header and column names.

* If your data does not have a header column, set the ``Header`` field to ``false`` when defining the Dataset.
