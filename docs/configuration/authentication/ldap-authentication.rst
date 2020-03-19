LDAP Authentication
===================

Fire Insights can be configured to authenticate the user against LDAP. Users have to be added to Fire, before they can log into Fire and start using it.

The following configurations have to be set appropriately.

.. figure:: ../_assets/installation/ldap-order.png
   :scale: 100%
   :alt: Sparkflows Ldap Order
   :align: center
   

LDAP Parameters
---------------


.. list-table:: LDAP Parameters
   :widths: 10 30 15
   :header-rows: 1

   * - Name of Parameter
     - Description
     - Example
   * - ldap.Order
     - Order in which to authenticate the user. Possible values are DB, LDAP_DB, DB_LDAP.
     - 
   * - ldap.URL
     - The URL of the LDAP server. The URL must be prefixed with ldap:// or ldaps://. The URL can optionally specify a custom port, for example: ldaps://ldap_server.example.com:1636.
     - ldap://localhost:10389
   * - ldap.Base
     - The distinguished name to use as a search base for finding users and groups. This should be similar to ‘dc=sparkflows,dc=com’.
     - dc=sparkflows,dc=com
   * - ldap.UserDn
     - Distinguished name of the user to bind as. This is used to connect to LDAP/AD for searching user and group information. This may be left blank if the LDAP server supports anonymous binds.
     - uid=john,ou=development,dc=sparkflows,dc=com
   * - ldap.Password
     - The password of the bind user.
     - xyz
   * - ldap.UserSearchBase
     - User Search Base
     - ou=development
   * - ldap.UserSearchFilter
     - The base filter for searching for users. For Active Directory, this is typically ‘(objectClass=user)’.
     - For Active Directory : (objectClass=user)     Other Example : (uid={0})
   * - ldap.GroupSearchBase
     - Group Search Base
     - ou=groups
   * - ldap.GroupSearchFilter
     - Group Search Filter
     - For Active Directory : (objectClass=group)     Other Example : (member={0})
     
Note
----

For ``ldap.UserSearchFilter`` we can use strings like ``(uid={USERNAME})``  
In this case {USERNAME} would be replaced by the real username of the user when searching in LDAP during ``Add User``.
     
LDAP Certificate
----------------

If ``ldaps`` is being used, the ldap certificate needs to be imported into cacerts.

For Reference : https://docs.oracle.com/cd/E19509-01/820-3399/ggfrj/index.html

Importing a user from LDAP into Fire
------------------------------------------

Once LDAP is enabled in Fire, users can be imported into Fire from LDAP.

* Go to Administration/User
* Click on Add/Sync User
* Enter the username and click on Search
* User details are fetched from LDAP
* Click on Add User to create the user in Fire

User Login
----------

Once LDAP is enabled in Fire, all the authentication for login in Fire are done against LDAP.

Search Order
-----

Fire would search in LDAP and then in its DB. Search order is determined by the parameter ldap.Order.

If it is set to ``LDAP_DB``, it would first search for the User in LDAP and then in its own DB. This allows having the admin user in the Fire DB if needed, so that all users are not locked out of the system in case LDAP goes down or ends up with invalid Configurations.

Reference
---------

Below are some great links for reference:

* Active Directory Search Filter Syntax : https://msdn.microsoft.com/en-us/library/aa746475(v=vs.85).aspx

What if I get locked out
------------------------

``ldap.Order`` determines the order in which Fire tries to log in the user.
In case you are locked out of Fire and are not able to log in, you can do the following:

* Add the below line to conf/configuration.properties::

    ldap.Order=DB

* Then restart the fire server. Now you should be able to log in with your admin account.

Once things are back to normal, you can remove the line you added to ``configuration.properties`` and restart the fire server.




Notes
-----

* Search strings are not case sensitive

