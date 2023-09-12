Overview
========

The RPB platform is a web-based solution which supports collection and exchange of radiotherapy specific research data
in large scale multi-centre clinical and pre-clinical studies. It delivers a study management and electronic data
capture system with special extensions dedicated to secure upload of medical imaging and treatment plans in DICOM format.

Getting Started
----------------

This section explains how to log in, change your current active study and be aware of changes happening in RPB IT
infrastructure.

Log In to Portal
^^^^^^^^^^^^^^^^

To access the RPB platform, in your web browser go to the RPB-portal home page. If you do not know the URL address,
please contact the local administrator of RPB at your site.

.. figure:: /img/login.png
	:name: img-login
	:alt: Login screen.

	Login screen.

In order to navigate to the RPB login form, please click on first login link on the page as it is highlighted in
the :numref:`img-login`. Afterwards you will be asked to provide your authentication credentials
(user name and password) which will grand you role based access to the RPB features. The minimal permission of
user is ROLE_USER.

.. note::
	RPB provides multiple authentication methods. The default way is to use the RPB EDC user account. With this account
	user can access complete range of RPB features (e.g. study as well as imaging data). However RPB is modular and
	could be deployed also to the environment without EDC (with limited functionality), e.g. when different EDC system
	is used. For such a scenarios the user will have to connect with different authorisation method. It is also possible
	to use LDAP based user authentication.

Change a Current Active Study
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When you use RPB, you usually work within a scope of specific study and partner site. The name of the current active
study is visible above the main menu at left side of the screen. In order to change the active study you have to click
on the name of the active study in top menu, see :numref:`img-change-study`.

.. figure:: /img/change-study.png
	:name: img-change-study
	:alt: Change active study menu.

	Change active study menu.


User Profile
^^^^^^^^^^^^

You can access your RPB user profile details by clicking on the link with your username in the right upper section of
the portal page as shown in :numref:`img-profile`. In addition to properties of your account, you can check as well
which permissions are activated for your account (User Roles) as well as list the audit log summarising audit events
that have been executed via your user account (Audit Logs).

.. figure:: /img/rpb-profile.png
	:name: img-profile
	:alt: User profile page.

	User profile page.

Read RSS news
^^^^^^^^^^^^^

RPB has a simple RSS module, :numref:`img-rss`, where users with necessary permissions can publish important news
about development and maintenance of particular RPB platform instance. This news are shown at the RPB home page, to
get there just click on the Home option in main menu at the lefts side of the screen.

.. figure:: /img/rpb-rss.png
	:name: img-rss
	:alt: RSS news feed.

	RSS news feed.

.. note:: 
	There is also a direct link to the RSS news feed in the footer of RPB portal page. This link can be used to
	subscribe for RSS news updates from standard RSS viewer software.

Log Out
^^^^^^^

To log out from RPB, click Logout link in the right upper section of the portal page as shown in :numref:`img-logout`.

.. figure:: /img/logout.png
	:name: img-logout
	:alt: Logout action link.

	Logout action link.

Portal Page Layout
------------------

The layout of RPB portal main page is separated to several areas with predefined features. Every page contains of the
following areas depicted in :numref:`img-page-layout`:

a) Top of page (Header),
b) Top menu (Below the header),
c) Main menu (Left side),
d) Body of page,
e) Bottom of page (Footer)

.. figure:: /img/page-layout.png
	:name: img-page-layout
	:alt: RPB portal page layout.

	RPB portal page layout.

Top of Page
^^^^^^^^^^^

The top of the page is the header area of the page. It contains (from left to right):

* RPB provider logo which navigates back to the RPB home page
* RPB provider partner site title
* Notification of logged user with login/ logout and home button

Top Menu
^^^^^^^^

Below the top page header there is a top menu. This menu consists of:

* Notification of current active study/site for user (left)
* Bread crumb for navigation for currently opened page

Main Menu
^^^^^^^^^

The main menu is located at left side of the screen. It consists from the tree structured menu items which points to the
concrete RPB modules. Which options are available depends on the type of logged user.

* Home
* CTMS - study management: clinical trial management module

	* Studies
	* Persons
	* Organisations

* EDC - data capture: electronic data capture module

	* Subjects/Events/CRFs
	* Randomisation
	* Study Data Import
	* Study Metadata

* PACS - medical imaging: picture archiving and communication in medicine module

	* Subjects/Events/DICOM
	* DICOM Lookup

* LAB - data tables: laboratory assays and tabulated data module

	* Study Data Update

* PID - patient identity: patient identity database module

	* Patient Search

* CMS - content management: news content module

	* RSS Articles

* Administration: system administration module

	* User Accounts

		* Roles
		* User Accounts

	* Configuration

		* Partner Sites
		* Software
		* Annotations
		* DICOM

			* RT-Struct Types
			* RT-Structs

	* Studiesmanagement

		* Studies
		* Study Phases
		* Study Statuses
		* Study Tag Types
		* Tumour Entities
		* Sponsoring Types
		* Study Timing
		* Document Types
		* Person Statuses
		* Timeline Event Types
		* Personnel Roles
		* Organisation Roles

	* AuditLogs

Body of Page
^^^^^^^^^^^^

What you see in the body of the page is depending on the module which you are accessing.

Bottom of Page
^^^^^^^^^^^^^^

The bottom of the page contains:

* Home: RPB portal home page
* Platform: RPB project web presence
* Licence: Software licensing details
* Software: List of software for download (RPB-client)
* Help: Link the on-line manual you are reading right now
* RSS: Direct link to RSS source for RPB portal
* Imprint: RPB platform provider details
* Privacy Policy: Data protection
* Contact: Send an email to RPB portal administration
* Version Number: RPB portal software version number
