Electronic Data Capture
=======================

.. note::
	The Electronic Data Capture (EDC) module is available only to users with ROLE_EDC_USER permission. The accessible
	studies need to be configured to use EDC component and linked with EDC studies (EDC-code study tag set to study
	unique code within the CTMS module).

Concept
-------

This module provides a web user interface to access the EDC system component integrated in RPB platform,
see :numref:`img-left-menu-edc`. The main functionality allows browsing studies/sites defined in EDC system and
enrolling new subjects using study specific pseudonymisation strategy.

.. figure:: /img/edc/left-menu-edc.png
	:name: img-left-menu-edc
	:alt: EDC module left menu items.

	EDC module left menu items.


Subjects/Events/CRFs
--------------------

.. note::
	ROLE_EDC_USER permission is needed to access this view. It does not currently operate within the scope of currently
	active study/site, but allows users to quickly switch between project without changing active study.

The project structure of EDC studies defined in RPB platform is limited to two levels. The top parent study level
holds all subjects enrolled in particular research project, whereas the second site level is limited to patients that
e.g. originates for one concrete partner site in the scope of multi-centre trial or are of specific characteristics such
as treated tumour entity within the scope of mono-centre trial. Even pure mono-centre trials usually have one site defined
that contains all study subjects. The project rights permissions in RPB components allows users to defined access based on
these two level hierarchy.

.. note::
	Additionally abstract sites such as DELETED and DUMMY are sometimes also used to control visibility of patients in the
	project and logically separate the access to the data.

.. toctree::
   :maxdepth: 1
   :caption: Tasks:

   change-study-site

View study/site configuration
Display enrolled subjects
Register new study subject
Re-identify study subject

Randomisation
-------------

.. note::
	ROLE_EDC_RANDOMISE permission is needed to allow subject randomisation. This view operates within the scope of
	currently active study/site.

Randomise Study Subject
Visualise Arm Assignments

Study Metadata
--------------

.. note::
	ROLE_EDC_METADATA permission is needed to allow the listing of study metadata items. This view operates within
	the scope of currently active study/site.

List all data items from eCRFs
