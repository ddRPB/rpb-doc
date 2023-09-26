Electronic Data Capture
=======================

.. note::
	The Electronic Data Capture (EDC) module is available only to users with ROLE_EDC_USER permission. The accessible
	studies need to be configured to use EDC component.

Concept
-------

This module provides a web user interface to access the EDC system component integrated in RPB platform,
see :numref:`img-left-menu-edc`. The main functionality allows browsing studies/sites defined in EDC system and
enrolling new subjects using study specific pseudonymisation strategy.

.. figure:: /img/edc/left-menu-edc.png
	:name: img-left-menu-edc
	:alt: EDC module left menu items.

	EDC module left menu items.

Open EDC
--------

.. note::
	ROLE_EDC_OPEN permission is needed to display the link for direct jump into the standalone EDC component.

From portal it is possible to directly navigate to standalone EDC system that is used for the actual eCRF study data
collection. These redirection link is visible in top left menu as depicted in :numref:`img-open-edc`.

.. figure:: /img/edc/open-edc.png
	:name: img-open-edc
	:alt: Open EDC direct link to jump into standalone eCRF collection application.

	Open EDC direct link to jump into standalone eCRF collection application.

Subjects/Events/CRFs
--------------------

.. note::
	ROLE_EDC_USER permission is needed to access this view. It does not currently operate within the scope of currently
	active study/site, but allows users to quickly switch between project without changing active study.

Partner Sites
^^^^^^^^^^^^^

This tab presents the project structure of EDC studies defined in RPB platform is limited to two levels, see :numref:`img-edc-studies-sites`.
The top parent study level holds all subjects enrolled in particular research project, whereas the second site level is
limited to patients that e.g. originates for one concrete partner site in the scope of multi-centre trial or are of
specific characteristics such as treated tumour entity within the scope of mono-centre trial. Even pure mono-centre
trials usually have one site defined that contains all study subjects. The project rights permissions in RPB components
allows users to defined access based on these two level hierarchy.

.. figure:: /img/edc/edc-studies-sites.png
	:name: img-edc-studies-sites
	:alt: EDC module study/sites hierarchy.

	EDC module study/sites hierarchy.

.. note::
	Additional abstract sites such as DELETED and DUMMY are often used to control visibility of patients in the
	project and logically separate the access to the data.

.. toctree::
	:maxdepth: 1
	:caption: Tasks:

	view-study-configuration
	change-study-site

Subjects
^^^^^^^^

This tab gets loaded when specific parent study and study site was selected in *Partner Sites* tab and will
provide and study subjects enrollment overview, :numref:`img-edc-subjects`.

.. figure:: /img/edc/edc-subjects.png
	:name: img-edc-subjects
	:alt: EDC module study subjects enrollment table.

	EDC module study subjects enrollment table.

.. toctree::
	:maxdepth: 1
	:caption: Tasks:

	enroll-subjects
	reidentify-subject

Events
^^^^^^

This tab gets loaded when specific study subject was selected in *Subjects* tab and will list study events that are
available for selected study subject in EDC system in order to allow certain set of administrative operations. Currently
this tab view is mostly useful for data managers.

.. toctree::
	:maxdepth: 1
	:caption: Tasks:

	reorder-repeating-events

Documents
^^^^^^^^^

This tab gets loaded when specific parent study as well as study site was selected in *Partner Sites* tab and will
provide access to documents associated with CTMS record of parent study.

.. toctree::
	:maxdepth: 1
	:caption: Tasks:

	download-study-document

Randomisation
-------------

.. note::
	ROLE_EDC_RANDOMISE permission is needed to allow subject randomisation. This view operates within the scope of
	currently active study/site.

Randomise Study Subjects
Visualise Arm Assignments

Study Metadata
--------------

.. note::
	ROLE_EDC_METADATA permission is needed to allow the listing of study metadata items. This view operates within
	the scope of currently active study/site.

List all data items from eCRFs
