Platform Introduction
=====================

The platform design was motivated by a need of linkage of research data that would have been otherwise managed
separately within dedicated databases (e.g.: clinical, imaging, laboratory). This linkage is possible if defined
naming and configuration conventions (data management strategy) are followed when setting up research projects.
RPB platform is therefore in no means a fully generic configurable solution, but it rather provides opinionated
selection of software system components and data integration use cases which have been found useful in
academic clinical research field. This platform is not a turn-key system that is operational out-of-the-box.
The following is the overall high level view on the platform architecture:

Standard Components
-------------------

* exposing standard or system specific API endpoints
* defining component and project specific data models

Integration Core
----------------

* defines radiotherapy research data model
* contains modules that give modality based access to linked data
* persists infrastructure model of integrated software components
* persists the core research project management data
* implements the integration between components and the radiotherapy research data model

Custom Applications
-------------------

* web portal for accessing the platform
* mobile app for tablet friendly data collection
* client/uploader for de-identification and upload of imaging and treatment planning data
* platform exposed API endpoints
