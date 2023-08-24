Medical Imaging
===============

The Medical Imaging (PACS) module is available only to users with ROLE_PACS_USER permission.

Concept
-------


To fullfill the specific requirements for using Medical Images in research, RadPlanBio has a concept of three states.

.. image:: ../img/pacs/image_data_states.png

Usually, data origin from the clinical system, where it is used for threatment. 

- First step is to pick the data that can be used for reasearch and pseudonymize it. Access to the hospital PACS system is necessary for that. The data will be pseudonymized, only.
- In a second step data will be picked for the project. No access to a hospital system is necessary. Data will be threated based on the project regulations.

That procedure ensures to fullfill the all regulations and allows user whithout permission for the clinical systems to do research on already pseudonymized data.


Tasks
-----

- `Transfer DICOM data from the hospital system to Study0 <hospital-data-to-study-zero-task.rst>`_
- Transfer DICOM data from Study0 to the project specific state
- Assign DICOM data to a specific event
