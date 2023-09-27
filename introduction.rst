Platform Introduction
=====================

.. warning:: RPB platform is not a turn-key system that is operational out-of-the-box. It rather requires intensive
	configuration and continuous operative data management activities.

The platform design was motivated by a need of linkage of research data that would have been otherwise managed
individually within dedicated databases (e.g.: clinical, imaging, laboratory). This linkage is possible if defined
naming and configuration conventions (data management strategy) are followed when setting up research projects.
RPB platform, see :numref:`img-rpb-building-blocks`, is therefore in no means a fully generic configurable solution,
but it rather provides opinionated selection of software system components and data integration use cases which have
been found useful in the scope of academic clinical studies. The following is the overall high level view on the platform infrastructure:

.. figure:: /img/rpb-building-blocks.png
	:name: img-rpb-building-blocks
	:alt: High level platform infrastructure overview.

	High level platform infrastructure overview.

Standard Components
-------------------

* standalone web applications and API endpoints
* implement project specific data models (per study)
* persist project research data (per subject)
* Open/LibreClinica, Conquest, LabKey

Integration Core
----------------

* defines radiotherapy research data model
* contains domains that give modality based access to linked data
* persists infrastructure model of integrated software components
* persists the core project management/ administrative data

Custom Applications
-------------------

* web portal for accessing the platform
* mobile webapp for mobile friendly data collection
* tools for de-identification and upload of DICOM data
* platform exposed API endpoints
