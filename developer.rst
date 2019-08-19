Developer Documentation
=======================

Information about RPB development and contribution worklfows. This documentation includes initial proposal for organising development activities.

Version Control
---------------

Git version control system is used for tracking changes in RPB project repositories. Those are hosted publicly via `ddRPB - RadPlanBio platform <https://github.com/ddRPB>`_ organisation. 

Repository
----------

`RPB platform <https://github.com/ddRPB/rpb>`_ (origin) is public repository for main RPB components (core, portal, mobile).

Issue Management
----------------

GitHub integrated issues management should be used to creates tickets before any code contributions. Tickets assigned to milestones that reflect the RPB software versioning scheme.

Conventional Commits
--------------------

Proposed is lightweight semantic conventions called `Conventional Commits <https://www.conventionalcommits.org>`_ for messages that make automation easier and correspond to proposed release versioning.

* `Cheat Sheet <https://www.cheatography.com/albelop/cheat-sheets/conventional-commits/pdf/>`_

Build
-----

Java 7
^^^^^^

To enable TLS 1.2 protocol with Java property

.. code-block:: bash
	:caption: Enable TLS 1.2 in maven build

	mvn -Dhttps.protocols=TLSv1.2

The same error for ant can be solved by this way

.. code-block:: bash
	:caption: Enable TLS 1.2 in ant build

	java -Dhttps.protocols=TLSv1.2 -cp %ANT_HOME%/lib/ant-launcher.jar org.apache.tools.ant.launch.Launcher

Tags
----

Tags should be created for released RPB components versions.

Release Versioning
------------------

Propsed is `Semantic Versioning <https://semver.org/>`_:

* MAJOR.MINOR.PATCH

Documentation
-------------

`reStructuredText <https://en.wikipedia.org/wiki/ReStructuredText>`_ (.rst) lightweight markup language is proposed to be used for the purpose of documentation writing. The RPB documentation source files reside in `rpb-doc <https://github.com/ddRPB/rpb-doc>`_  repository. This repository contains a webhook to trigger the re-build of static HTML resources that are publicly hosted via `Read the Docs <https://readthedocs.org/>`_ (RTD) utilising RTD Sphinx Theme.