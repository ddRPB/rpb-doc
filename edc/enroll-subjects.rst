Enroll New Study Subjects
=========================

.. note::
	ROLE_EDC_SUBMIT permission is needed to allow the subject enrollment into selected study site. Additionally if
	study and partner site is configured to used pseudonym generator, ROLE_PID_NEW will allow the user to generate
	new patient pseudonym from identifiable data.

In order to register new subject into projects within RPB, it is always necessary to assign two identifier to the subject.
How these identifier are assigned depend on specific partner site and study configuration. However what always holds true
is that first identifier (*Study Subject ID*) need to be unique for subject in the scope of project and the second identifier
(*PID - pseudonym*) needs to be globally unique for subject inside RPB database.

The subject enrollment dialog is available withing the *Subjects* tab of *Subjects/Events/CRFs* view after selection of
study site, :numref:`img-edc-subjects-new`.

.. figure:: /img/edc/edc-subjects-new.png
	:name: img-edc-subjects-new
	:alt: EDC module and enrollment of new subject.

	EDC module and enrollment of new subject.

The actual enrollment dialog adapts based on configuration, however the following covers some of the typical scenarios.

Using Pseudonym Generator
-------------------------

When partner site has pseudonym generator configured and identity management is enabled for the study, the enrollment dialog
follows the below workflow, see :numref:`img-edc-idat-pid`:

1.	The Study Subject ID is manually provided by data entry person together with the rest of properties such as enrollment
	date and subject gender.

2.	The user should provide subject identity data (name, surname, birthdate) for the purpose of pseudonym generation. The optional
	additional data (place or residence, ZIP code and birthname) are also recommended to enter if they are available for data entry personnel
	in order to guarantee uniqueness of generated PID.

3.	Generation is triggered by clicking on *Generate* button.

4.	When PID generation is successful, it gets displayed next to the *PID* label. Afterwards it is possible to click on *Submit*
	button that triggers the enrollment into study site. On enrollment will the pseudonym be prefixed with partner site identifier to denote
	explicitly the scope of PID uniqueness.

.. figure:: /img/edc/edc-idat-pid.png
	:name: img-edc-idat-pid
	:alt: Unique subject pseudonym derived from identity data.

	Unique subject pseudonym derived from identity data.


Without Pseudonym Generator
---------------------------

When partner site has no pseudonym generator configured or identity management is disabled for the study, the enrollment dialog
follows the below workflow, see :numref:`img-edc-auto-pid`:

1.	The Study Subject ID is manually provided by data entry person together with the rest of properties such as enrollment
	date and subject gender.

2.	Leaving the Study Subject ID text box will trigger the autogeneration of pseudonym. In this case there is no identity
	management happening in RPB and site needs to keep patient re-identification list outside of scope of RPB platform.

3.	It is now possible to click on *Submit* button that triggers the enrollment into study site. One can see that the pseudonym
	derived from Study Subject ID is prefixed with partner site identifier and study EDC-code to ensure the uniqueness in scope of
	RPB database.

.. figure:: /img/edc/edc-auto-pid.png
	:name: img-edc-auto-pid
	:alt: Unique pseudonym derived from Study Subject ID.

	Unique subject pseudonym derived from Study Subject ID.


Selecting from Internal Registry
--------------------------------

This option is only relevant for provider of RPB platform that is also hosting internal patient registry that aggregates
patient eligible for enrollment into prospective and retrospective studies. In this scenario the subjects are pseudonymised
prior (often automatically) and user can then select the subject for enrollment knowing the Study Subject ID that is used in
the internal patient registry. The enrollment dialog follows the below workflow, see :numref:`img-edc-s0-pid`:

1.	The Study Subject ID is manually provided by data entry person together with the rest of properties such as enrollment
	date and subject gender.

2.  Data entry person can select subject by searching the Study Subject ID from special internal registry.

3.	Pseudonym gets loaded and if user has *ROLE_REIDENTIFY* permission the selected subject identity gets displayed for
	confirmation.

4. It is now possible to click on *Submit* button that triggers the enrollment into study site.

.. figure:: /img/edc/edc-s0-pid.png
	:name: img-edc-s0-pid
	:alt: Unique pseudonym selected from internal registry.

	Unique subject pseudonym selected from internal registry.
