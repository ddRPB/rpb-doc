Explaining Subject ID Types
===========================

At this place it is important to explain that there are three main types of subject identifiers which are used in RPB.
Each of the type has its own purpose and one should understand what is the meaning of it:

* 	*Study Subject ID*: is identifying subject within one study. It can be automatically generated or manually specified
	(depending on EDC study configuration). One patient taking part in multiple studies will have
	different Study Subject ID in each study. This ID has nothing to do with patient identity and cannot be use to obtain
	first or last name of patient.

* 	*PID - pseudonym*: is a unique identifier of the patient in RPB platform. One patient taking part in multiple studies
	will have the same PID in each one of them. It is generated from patient identity data (first name, last name, etc.)
	by patient identity management system in RPB. It is possible to not to use identity management system and manually
	provide PID, but in this case one has to guarantee the uniqueness of PID per patient and store the identity association
	somewhere outside of RPB. PID is also used in case of DICOM Patient ID tag when DICOM imaging data are de-identified.

* 	*Secondary ID*: sometimes it is useful to store patient ID from different systems and associate this ID to our study
	subject. And for this case we have a possibility to use this Secondary ID field.
