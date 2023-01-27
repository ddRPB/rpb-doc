Monitoring Health
=================

The platform components are standalone systems that expose the API for the purpose of software integration. These APIs
are actively used and failure of one or more of APIs will result in partial or complete breakage of the platform functionality.
These types of interfaces are important for the correct operation of the platform:

- Web Services (e.g. REST, SOAP, WebDAV, DICOMweb)
- DICOM Communication
- HL7 Communication
- LDAP/ LDAPs
- SMTP/ SMTPs

Most of the web services need to be reachable from outside (with help of reverse proxy) as well as from inside organisation.

DICOM and HL7 communication is typically restricted to inside communication only and are not exposed to external sites.

The same applies for LDAP which is used for authentication against central Active Directory and SMTP/ SMTPs communication
to allow certain components to generate email messages. If LDAPs or SMTPs is configured, one should monitor the expiration of
SSL certificates of central LDAP and SMTP infrastructure because expiration of certificate will require its reimport to
certificate stores of particular application to gain trust and re-enable broken communication.

Web Services
------------

Server - legacy
^^^^^^^^^^^^^^^

Login: return JSON of logged in user if success

- serveriePartnerSiteIdentifier
- rpbuser
- sha1passwordhash
- radplanbio.url.de

.. code-block:: bash

    wget -d --header="Content-Type: application/json" --header="Username: rpbuser" --header="Password: sha1passwordhash" https://radplanbio.url.de/serveriePartnerSiteIdentifier/api/v1/getMyDefaultAccount/

Portal
^^^^^^

Hello: testing the reachability to the portal API endpoint

.. code-block:: bash

    wget -d https://radplanbio.url.de/api/hello/ping

RSS: RSS/atom stream of the portal

.. code-block:: bash
    :caption: Retrieving portal RSS stream

     wget -d --header="Content-Type: application/rss+xml; charset=utf-8;" https://radplanbio.url.de/api/rss

WebDAV: WebDAV interface

.. code-block:: bash
    :caption: Listing study folders

     davix-ls https://radplanbio.url.de/api/v1/webdav/studies --userlogin rpbapikey --userpass anything

DICOMweb: DICOMweb interface

.. code-block:: bash
    :caption: Storing DICOM instances into research PACS (STOW-RS), clinical trial agnostic

     https://radplanbio.url.de/api/v1/dicomweb/studies

OpenClinica/ LibreClinica
^^^^^^^^^^^^^^^^^^^^^^^^^

SOAP:

List studies: used also to check if user has SOAP access to EDC system and lists available studies

- request.xml (SOAP XML need to be constructed prior)

.. code-block:: XML

    <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:v1="http://openclinica.org/ws/study/v1">
     <soapenv:Header>
      <wsse:Security soapenv:mustUnderstand="1" xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
       <wsse:UsernameToken wsu:Id="UsernameToken-27777511" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">
        <wsse:Username>rpbuser</wsse:Username>
        <wsse:Password type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordText">sha1passwordhash</wsse:Password>
       </wsse:UsernameToken>
      </wsse:Security>
     </soapenv:Header>
     <soapenv:Body>
      <v1:listAllRequest/>
     </soapenv:Body>
    </soapenv:Envelope>

- radplanbio.url.de

.. code-block:: bash

    wget -d --post-file=request.xml --header="Content-Type: text/xml; charset=utf-8;" --header "SOAPAction:v1:listAllRequest" https://radplanbio.url.de/OpenClinica-ws/ws/study/v1/studyWsdl.wsdl

Conquest
^^^^^^^^

CTP
^^^

Mainzelliste
^^^^^^^^^^^^

Enketo
^^^^^^

LabKey
^^^^^^

DICOM Communication
-------------------

For DICOM communication both parties/ application entities (calling and called) need to be properly configured to recognise each other. It requires giving each
party unique name (application entity title - AET). Hostnames are normally not used in DICOM communication. The IP addresses and ports need to be specified and
the internal communication need to be open for those.

Conquest
^^^^^^^^

CTP
^^^

Weasis/ Viewer
^^^^^^^^^^^^^^

- find in Conquest (C-FIND)
- query and retrieve from Conquest (C-MOVE)
- store in Pseudo-Master CTP pipeline (C-STORE)

HL7 Communication
-----------------

Deployment specific HL7 listener channels for messages from central HL7 communication host (e.g. ADT and BAR messages).

Mirth/ NextGen Connect
^^^^^^^^^^^^^^^^^^^^^^

HL7 port need to be open for internal communication and the central HL7 communication host reachable from he machine where the component is installed.

LDAP/ LDAPs
-----------

LDAP/ LDAPs port need to be open for internal communication and the central LDAP/ LDAPs host reachable from the machine where particular component
is installed. LDAP service user account is needed for LDAP bind operation. If encrypted version is used the certificate of the LDAPs host need to be
imported in certificate store of particular components (e.g. Java keystore).

Portal
^^^^^^

- authentication

OpenClinica/ LibreClinica
^^^^^^^^^^^^^^^^^^^^^^^^^

- authentication

LabKey
^^^^^^

- authentication

SMTP/ SMTPs
-----------

SMTP/ SMTPs port need to be open for internal communication and the central SMTP/ SMTPs host reachable from the machine where particular component
is installed. LDAP service use account may be needed as some organisations allow only authenticated SMTP communication.
If encrypted version is used the certificate of the SMTPs host need to be imported in certificate store of
particular component (e.g. Java keystore).

Portal
^^^^^^

- email notifications/ messages

OpenClinica/ LibreClinica
^^^^^^^^^^^^^^^^^^^^^^^^^

- email notifications/ messages

LabKey
^^^^^^

- email notifications/ messages

CTP
^^^

- email notifications/ messages
