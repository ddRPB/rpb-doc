Explaining Subject ID Types
===========================

At this place it is important to explain that there are three main types of subject identifiers which are used in RPB.
Each of the type has its own purpose and one should understand what is the meaning of it:

* 	*Study Subject ID* (mandatory): is identifying subject within one concrete study. It can be automatically generated or manually
	specified (EDC study configuration). One patient taking part in multiple studies will have
	different Study Subject ID in each study.

* 	*PID - pseudonym* (mandatory): is a unique identifier of the patient in RPB platform. One patient taking part in multiple studies
	will have the same PID in each one of them (allows subject tracking across studies). It is generated from patient
	identity data (first name, last name, etc.) by patient identity management system in RPB. It is also possible to not
	use identity management system and manually provide PID, but in this case one has to guarantee the uniqueness of PID
	per patient and store the identity association somewhere outside of RPB. PID is also used in case of DICOM Patient ID
	tag when DICOM imaging data are de-identified. In RPB every subject pseudonym is prefixed with partner site identifier.

* 	*Secondary ID* (optional): sometimes it is useful to store patient ID from different systems and associate this ID to our study
	subject. And for this case we have a possibility to use this Secondary ID field.

.. note::
	PID can be also created from Study Subject ID automatically (when PID generator is not used). In such case tracking
	subject across studies is not possible.
