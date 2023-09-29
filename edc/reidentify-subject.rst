Re-identify Study Subject
=========================

.. note::
	ROLE_REIDENTIFY permission is needed to allow subject re-identification.

When RPB PID generator was used to pseudonymise the subject enrolled in specific study site, the users of that specific
partner site can re-identify the subject. This simple workflow is accessible from the *Subjects* tab of *Subjects/Events/CRFs* view,
see :numref:`img-edc-subject-reidentify`:

1.	Clicking *Edit* button in *Subjects* data table will display the *Edit Dialog*.

2. 	If proper PID was used and necessary user permissions are granted the *Reidentify* button is enabled and can be triggered.

3.	Subject identity gets loaded from identity management database (this action creates and audit log entry).

.. figure:: /img/edc/edc-subject-reidentify.png
	:name: img-edc-subject-reidentify
	:alt: Reidentify pseudonymised subject enrolled in specific study site.

	Reidentify pseudonymised subject enrolled in specific study site.
