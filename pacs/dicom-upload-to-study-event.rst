DICOM Upload to Study Event
===========================

Task Description
----------------

You want to link DICOM data to a specific study event of a specific subject.

Therefore:

- you need to select the study subject
- select the event
- (upload DICOM data)
- assign DICOM data to upload slot

Prerequisits
------------

- DICOM data are uploaded to Study0 (if site is fully integrated in the RPB Infrastructure)
- DICOM data are available for upload with the Upload Client
- Subject is enrolled in your study
- Events and upload slots are defined in the EDC system

Tasks
-----

1. `Preparation`_
2. `Select the Subject`_
3. `Select the Event`_
4. `Upload DICOM Data`_
5. `Assign Existing DICOM Data`_


Preparation
^^^^^^^^^^^

It is important to verify that your Study is active. If you are in a different Study read `here <../overview/overview.rst#change-a-current-active-study>`_ how to change that.

In the menu, navigate to "PACS - medical imaging" -> "Subjects/Events/DICOM".

.. image:: ../img/pacs/DICOM-Upload-to-Study-Event/prepare-upload-to-study-event.png
   :width: 900pt

Select the Subject
^^^^^^^^^^^^^^^^^^

First step is to pick the study subject (patient). A click on the table item loads the events for the subject. The notification in the right upper corner shows that.

.. image:: ../img/pacs/DICOM-Upload-to-Study-Event/select-subject.png
   :width: 900pt

Select the Event
^^^^^^^^^^^^^^^^

Switching to the "Events" tab opens the next view. There you can see available events of the subject. Clicking on the events loads the DICOM data that are already assigned.

.. image:: ../img/pacs/DICOM-Upload-to-Study-Event/select-event.png
   :width: 900pt

Upload DICOM Data
^^^^^^^^^^^^^^^^^



Assign Existing DICOM Data
^^^^^^^^^^^^^^^^^^^^^^^^^^