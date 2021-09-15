Laboratory Data (LAB)
=====================

RPB integrates with LabKey 17.3 Laboratory Data Management system which is used as storage tabulated data in order to data post-processing, search and reporting.


==================== ======== ================== ==============
OS                   Init     Application Server Database      
==================== ======== ================== ==============   
Debian 9 (Stretch)   System V JDK 8, Tomcat 8    PostgreSQL 9.6
==================== ======== ================== ==============


PostgreSQL
----------

- Port: 5432
- Locale: UTF8
- Root user: postgres

.. code-block:: bash
	:caption: Create labkey role and labkey database

	psql -U postgres -c "CREATE ROLE labkey LOGIN ENCRYPTED PASSWORD 'labkey' SUPERUSER NOINHERIT NOCREATEDB NOCREATEROLE"
	psql -U postgres -c "CREATE DATABASE labkey WITH ENCODING='UTF8' OWNER=labkey"

	