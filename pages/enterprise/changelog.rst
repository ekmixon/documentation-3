*********
Changelog
*********

Graylog Enterprise 4.1.3
========================

Released: 2021-08-04

Enterprise
----------

No changes since 4.1.2.


Graylog Enterprise 4.1.2
========================

Released: 2021-07-28

Enterprise
----------

**Security**

Session ID leak in Graylog DEBUG log file and audit log.

We recently discovered a session ID leak in the Graylog DEBUG log file as well as the audit log. A user can use a session ID to authenticate against Graylog and then this user has access to all the permissions associated with the owner of the session ID.

The ID was printed in DEBUG level log messages (DEBUG is not enabled by default) as well as the Graylog Enterprise Audit Log. By default, the Graylog Audit Log is only logging to the local database and only accessible by Graylog administrators.

We would like to thank David Herbstmann for discovering and responsibly disclosing this vulnerability.

The following CVE IDs have been assigned: `CVE-2021-37759 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37759>`_, `CVE-2021-37760 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37760>`_

**Fixed**

- Fix license check issue in LogView widget. `Graylog2/graylog2-server#10940 <https://github.com/Graylog2/graylog2-server/issues/10940>`_ `Graylog2/graylog-plugin-enterprise#2449 <https://github.com/Graylog2/graylog-plugin-enterprise/issues/2449>`_


Graylog Enterprise 4.1.1
========================

Released: 2021-07-07

Enterprise
----------

**Fixed**

- Add default value for the spool directory in the UI configuration for the S3 archiving backend.
- Improve Forwarder request/response handling when server has high load.

Enterprise Integrations Plugin
------------------------------

**Added**

- Add lookup data adapter for abuse.ch ThreadDox IOC.


Graylog Enterprise 4.1.0
========================

Released: 2021-06-23

Enterprise
----------

**Added**

- Add theme customization options to allow the usage of custom colors.
- Add support for global notifications to display announcements and other messages to all users or a selected group of users.
- Add authentication and team-sync support for the Okta indentity provider.
- Add support for the Graylog Forwarder. The Graylog Forwarder is a standalone agent for sending log data to Graylog Cloud or an on-premise Graylog Server cluster.
- Add Log View widget including file export. This allows users to read log messages in a way similar to reading plain text log files.
- Add support for exporting messages in JSON, NDJSON and plain text formats.
- Add S3 archiving backend to store archives in AWS S3 compatible object stores.
- Add option to make archive batch size configurable for performance tuning.
- Extend search and dashboard parameters to allow pre-defined values based on static lists or available message field values.
- Add pagination for reports overview.

**Fixed**

- Improve archiving multiple indices.
- Fix rendering world map visualization in reports.
- Improved search and dashboard parameter validation and styling.
- Use case-insensitive matching for LDAP/AD group sync.
- Disable confusing traffic warning log messages by default.

Enterprise Integrations Plugin
------------------------------

**Added**

- Add ActiveDirectory user lookup data adapter.
- Add Enterprise Greynoise lookup data adapter.
- Add URLhaus lookup data adapter.


Graylog Enterprise 4.0.11
=========================

Released: 2021-08-04

Enterprise
----------

No changes since 4.0.10.


Graylog Enterprise 4.0.10
=========================

Released: 2021-07-28

Enterprise
----------

**Security**

Session ID leak in Graylog DEBUG log file and audit log.

We recently discovered a session ID leak in the Graylog DEBUG log file as well as the audit log. A user can use a session ID to authenticate against Graylog and then this user has access to all the permissions associated with the owner of the session ID.

The ID was printed in DEBUG level log messages (DEBUG is not enabled by default) as well as the Graylog Enterprise Audit Log. By default, the Graylog Audit Log is only logging to the local database and only accessible by Graylog administrators.

We would like to thank David Herbstmann for discovering and responsibly disclosing this vulnerability.

The following CVE IDs have been assigned: `CVE-2021-37759 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37759>`_, `CVE-2021-37760 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37760>`_


Graylog Enterprise 4.0.9
========================

Released: 2021-07-07

No changes since 4.0.8.


Graylog Enterprise 4.0.8
========================

Released: 2021-06-02

Enterprise
----------

**Fixed**

- Lower log level for irregular traffic record check.


Graylog Enterprise 4.0.7
========================

Released: 2021-05-05

Enterprise
----------

**Fixed**

- Fix rendering of the world map visualization in reports.


Graylog Enterprise 4.0.6
========================

Released: 2021-04-07

Enterprise
----------

**Fixed**

- Change LDAPGroupResolver to use case-insensitive matching

Enterprise Integrations Plugin
------------------------------

**Added**

- Add "drop sensitive data" option to Microsoft365 input

Graylog Enterprise 4.0.5
========================

Released: 2021-02-22

Enterprise
----------

No changes since 4.0.4.


Graylog Enterprise 4.0.4
========================

Released: 2021-02-22

Enterprise
----------

No changes since 4.0.3.


Graylog Enterprise 4.0.3
========================

Released: 2021-02-16

Enterprise
----------

No changes since 4.0.2.

Enterprise Integrations Plugin
------------------------------

**Added**

- Add full-message transformer to Enterprise Output Framework.


Graylog Enterprise 4.0.2
========================

Released: 2021-01-27

Enterprise
----------

**Added**

- Allow modification of timezone in report scheduling settings.

**Fixed**

- Fix report preview styling when dark mode is active.

Enterprise Integrations Plugin
------------------------------

**Fixed**

- Reduce noise of legacy script alarm callback notification.
- Fix timing issue with old checkpoints in Office365 plugin.
- Properly shut down TCP connections when stopping Enterprise outputs.


Graylog Enterprise 4.0.1
========================

Released: 2020-11-25

Enterprise
----------

No changes since 4.0.0.

Enterprise Integrations Plugin
------------------------------

- Do not shut down Okta input on errors.
- Let Office 365 plugin use configured proxy settings.


Graylog Enterprise 4.0.0
========================

Released: 2020-11-18

Enterprise
----------

**Added**

- Add support for grouping users in teams.

  - See: :ref:`Permission Management <permissions>`
- Add support for managing access to streams, searches and dashboards through teams.

  - See: :ref:`Permission Management <permissions>`
- Add support for syncing groups from LDAP and Active Directory into Graylog teams.

  - See: :ref:`Permission Management <permissions>`
- Add configurable header badge.
- Create notification for failed Enterprise outputs.
- Add cluster resources for archiving to allow archiving to be managed from all server nodes.

**Fixed**

- Don't fail reports migration if a widget is missing.
- Improve error logging for report generation.

Enterprise Integrations Plugin
------------------------------

**Added**

- Script event notification plugin to replace the legacy script alarm callback plugin.


Graylog Enterprise 3.3.14
=========================

Released: 2021-07-28

Enterprise
----------

**Security**

Session ID leak in Graylog DEBUG log file and audit log.

We recently discovered a session ID leak in the Graylog DEBUG log file as well as the audit log. A user can use a session ID to authenticate against Graylog and then this user has access to all the permissions associated with the owner of the session ID.

The ID was printed in DEBUG level log messages (DEBUG is not enabled by default) as well as the Graylog Enterprise Audit Log. By default, the Graylog Audit Log is only logging to the local database and only accessible by Graylog administrators.

We would like to thank David Herbstmann for discovering and responsibly disclosing this vulnerability.

The following CVE IDs have been assigned: `CVE-2021-37759 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37759>`_, `CVE-2021-37760 <https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-37760>`_


Graylog Enterprise 3.3.13
=========================

Released: 2021-05-05

Enterprise
----------

**Fixed**

- Fix rendering of the world map visualization in reports.


Graylog Enterprise 3.3.12
=========================

Released: 2021-04-14

No changes since 3.3.11.


Graylog Enterprise 3.3.11
=========================

Released: 2021-02-16

No changes since 3.3.10.


Graylog Enterprise 3.3.10
=========================

Released: 2021-01-27

Enterprise
----------

**Added**

- Allow modification of timezone in report scheduling settings.


Graylog Enterprise 3.3.9
========================

Released: 2020-11-25

Enterprise
----------

**Fixed**

- Fix audit formatting for file resource.
- Fix permission issue with reports.
- Fix logo images in reports.
- Fix issue with rendering help buttons.

Enterprise Integrations Plugin
------------------------------

**Fixed**

- Do not shut down Office 365 input on errors.
- Do not shut down Okta input on errors.
- Fix issue with Office 365 logon data parsing.
- Let Office 365 plugin use configured proxy settings.


Graylog Enterprise 3.3.8
========================

Released: 2020-10-12

Enterprise Integrations Plugin
------------------------------

**Fixed**

- Fixed an issue with the O365 codec where it was not handling the event timestamp correctly.


Graylog Enterprise 3.3.7
========================

Released: 2020-10-08

Enterprise Integrations Plugin
------------------------------

**Fixed**

- Ensure cleanup of on-disk journal when Enterprise Output is deleted.


Graylog Enterprise 3.3.6
========================

Released: 2020-09-28

Enterprise
----------

**Fixed**

- Improve error logging during report generation.

Enterprise Integrations Plugin
------------------------------

**Added**

- Add Google BigQuery output to the enterprise output framework.

**Fixed**

- Fix ``NullPointerException`` and thread-safety issues in the enterprise output framework.
- Fix retry logic and overall robustness of the office365 input.
- Improve error detection and error handling in the enterprise output framework.


Graylog Enterprise 3.3.5
========================

Released: 2020-08-17

**Fixed**

- Fix NullPointerException when deleting an output, which caused the on-disk journal to not get cleaned up.


Graylog Enterprise 3.3.4
========================

Released: 2020-08-06

**Changed**

- Fix pipeline selection on output creation to make the pipeline optional rather than required.

**Fixed**

- Fixed a bug which occurred during the setup of the O365 Input.
- Fix error when starting the Forwarder with the Enterprise Integrations plugin.


Graylog Enterprise 3.3.3
========================

Released: 2020-07-29

**Added**

- Add office365 input plugin.
- Add reliable output framework and TCP and TCP Syslog outputs.

Graylog Enterprise 3.3.2
========================

Released: 2020-06-24

**Fixed**

- Fix message table headers in reports.

Graylog Enterprise 3.3.1
========================

Released: 2020-06-10

**Fixed**

- Fix issue with reports database migration when widgets are missing.
- Add a cluster resource for the archiving HTTP API and use it in the UI. All endpoints in the cluster resource are routed to the regular endpoints on the master node to avoid the need for custom proxy configuration.

Graylog Enterprise 3.3.0
========================

Released: 2020-05-20

**Added**

- Input for Okta log events.
- Create detailed audit log messages for search jobs.
- Create detailed audit log messages for message exports.
- Automatically install trial licenses requested from the UI.
- Add 1 day mute option to trial license reminders.

**Changed**

- Implement message list limit in reports.

**Fixed**

- Fix archive catalog response with different backends having the same archive.
- Improve keyboard input for search/dashboard parameter fields.
- Improve error messages with missing parameters in reports.
- Fix problem with non-ascii characters in correlation field names.
- Fix unintended selection of multiple widgets in report widget selection.
- Fix detection of value-less parameters in reports.
- Hide license warning on search/dashboard page if no license is installed.
- Use user defined chart colors in reports.

Graylog Enterprise 3.2.6
========================

Released: 2020-06-10

No changes since 3.2.5.

Graylog Enterprise 3.2.5
========================

Released: 2020-05-19

No changes since 3.2.4.

Graylog Enterprise 3.2.4
========================

Released: 2020-03-19

**Fixed**

- Fix issue with search parameter input fields.
- Fix error exporting a correlation event definition in content packs.

Graylog Enterprise 3.2.3
========================

Released: 2020-03-11

**Fixed**

- Fix issue with custom fields and correlation event definitions.

Graylog Enterprise 3.2.2
========================

Released: 2020-02-20

**Fixed**

- Fix missing rows in message table widget in reports. `Graylog2/graylog2-server#7349 <https://github.com/Graylog2/graylog2-server/issues/7349>`_ `Graylog2/graylog2-server#7492 <https://github.com/Graylog2/graylog2-server/issues/7492>`_
- Don't try to archive indices which have already been archived.

Graylog Enterprise 3.2.1
========================

Released: 2020-02-04

**Fixed**

- Gracefully handle missing dashboards and widgets when collecting parameters for reports. `Graylog2/graylog2-server#7347 <https://github.com/Graylog2/graylog2-server/issues/7347>`_

Graylog Enterprise 3.2.0
========================

Released: 2020-01-14

**Added**

- Dynamic list support for events and alert definition queries.
- Search parameter support for reports.
- MongoDB lookup data adapter.

**Fixed**

- Remove incomplete archive directory when archiving process fails.
- Fix race condition with archive catalog writing.

Graylog Enterprise 3.1.4
========================

Released: 2020-01-14

**Fixed**

- Only write archive metadata if the archiving process succeeded.
- Improve resiliency of widgets in reports.

Graylog Enterprise 3.1.3
========================

Released: 2019-11-06


**Fixed**

- Fix problem with correlating events created by aggregation event definitions.
- Remove incomplete archive directory when archive job fails or is stopped.

Graylog Enterprise 3.1.2
========================

Released: 2019-09-12

No changes since 3.1.1.

Graylog Enterprise 3.1.1
========================

Released: 2019-09-04

No changes since 3.1.0.

Graylog Enterprise 3.1.0
========================

Released: 2019-08-16

**Added**

- Add correlation engine and UI for new alerts and events system.
- Add Enterprise job scheduler implementation.

**Removed**

- Moved views feature to open-source. (except parameter support)

**Fixed**

- Fix report service memory leak.
- Fix auto-completion in drop-down fields.
- Fix rendering of archive configuration page

Graylog Enterprise 3.0.2
========================

Released: 2019-05-03

**Integrations Plugin**

- Improve Graylog Forwarder configuration defaults.
- Improve Graylog Forwarder error handling.
- Update Graylog Forwarder dependencies.

Graylog Enterprise 3.0.1
========================

Released: 2019-04-01

- Fix missing authorization checks in the license management.
- Fix view sharing issue for regular users.
- Fix memory leak in the reporting system.

**Integrations Plugin**

- Add Graylog Forwarder feature.

Graylog Enterprise 3.0.0
========================

Released: 2019-02-14

- Announcement blog post: https://www.graylog.org/post/announcing-graylog-v3-0-ga
- Upgrade notes: :doc:`/pages/upgrade/graylog-3.0`

A detailed changelog is following soon!

**Integrations Plugin**

* Add Script Alert Notification

Graylog Enterprise 2.5.2
========================

Released: 2019-03-15

Plugin: License
---------------

- Add missing permissions to license HTTP API resources.
- Only show upcoming license expiration warning to admin users.

Graylog Enterprise 2.5.1
========================

Released: 2018-12-19

No changes since 2.5.0.

Graylog Enterprise 2.5.0
========================

Released: 2018-11-30

No changes since 2.4.6.

Graylog Enterprise 2.4.7
========================

Released: 2019-03-01

Plugin: License
---------------

* Add missing authorization checks to license resources.

Graylog Enterprise 2.4.6
========================

Released: 2018-07-16

No changes since 2.4.5.

Graylog Enterprise 2.4.5
========================

Released: 2018-05-28

No changes since 2.4.4.

Graylog Enterprise 2.4.4
========================

Released: 2018-05-02

No changes since 2.4.3.

Graylog Enterprise 2.4.3
========================

Released: 2018-01-24

No changes since 2.4.2.

Graylog Enterprise 2.4.2
========================

Released: 2018-01-24

No changes since 2.4.1.

Graylog Enterprise 2.4.1
========================

Released: 2018-01-19

No changes since 2.4.0.

Graylog Enterprise 2.4.0
========================

Released: 2017-12-22

No changes since 2.4.0-rc.2.

Graylog Enterprise 2.4.0-rc.2
=============================

Released: 2017-12-20

No changes since 2.4.0-rc.1.

Graylog Enterprise 2.4.0-rc.1
=============================

Released: 2017-12-19

No changes since 2.4.0-beta.4.

Graylog Enterprise 2.4.0-beta.4
===============================

Released: 2017-12-15

Plugin: License
---------------

* The license page now shows more details about the installed licenses.

Graylog Enterprise 2.4.0-beta.3
===============================

Released: 2017-12-04

No changes since 2.4.0-beta.2.

Graylog Enterprise 2.4.0-beta.2
===============================

Released: 2017-11-07

No changes since 2.4.0-beta.1.

Graylog Enterprise 2.4.0-beta.1
===============================

Released: 2017-10-20

Plugin: Archive
---------------

* Add support for Zstandard compression codec.

Graylog Enterprise 2.3.2
========================

Released: 2017-10-19

Plugin: Archive
---------------

* Fix archive creation for indices with lots of shards.

Graylog Enterprise 2.3.1
========================

Released: 2017-08-25

Plugin: Archive
---------------

* Lots of performance improvements (up to 7 times faster)
* Do not delete an index if not all of its documents have been archived

Graylog Enterprise 2.3.0
========================

Released: 2017-07-26

Plugin: Archive
---------------

* Record checksums for archive segment files
* Add two archive permission roles "admin" and "viewer"
* Allow export of filenames from catalog search

Graylog Enterprise 2.2.3
========================

Released: 2017-04-04

Plugin: Archive
---------------

* Metadata is now stored in MongoDB
* Preparation for storage backend support

Graylog Enterprise 2.2.2
========================

Released: 2017-03-02

Plugin: Audit Log
-----------------

* Extend integration with the Archive plugin

Graylog Enterprise 2.2.1
========================

Released: 2017-02-20

Plugin: Archive
---------------

* Improve stability and smaller UI fixes

Graylog Enterprise 2.2.0
========================

Released: 2017-02-09

Plugin: Archive
---------------

* Improve index set support

Graylog Enterprise 1.2.1
========================

Released: 2017-01-26

Plugin: Archive
---------------

* Prepare the plugin to be compatible with the new default stream.

Plugin: Audit Log
-----------------

* Add support for index sets and fix potential NPEs.
* Smaller UI improvements.

Graylog Enterprise 1.2.0
========================

Released: 2016-09-14

https://www.graylog.org/blog/70-announcing-graylog-enterprise-v1-2


Plugin: Archive
---------------

* Add support for selecting which streams should be included in your archives.


Plugin: Audit Log
-----------------

New plugin to keep track of changes made by users to a Graylog system by automatically saving them in MongoDB.


Graylog Enterprise 1.1
======================

Released: 2016-09-01

* Added support for Graylog 2.1.0.


Graylog Enterprise 1.0.1
========================

Released: 2016-06-08

Bugfix release for the archive plugin.

Plugin: Archive
---------------

Fixed problem when writing multiple archive segments
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There was a problem when exceeding the max segment size so that multiple archive
segments are written. The problem has been fixed and wrongly written segments
can be read again.

Graylog Enterprise 1.0.0
========================

Released: 2016-05-27

Initial Release including the Archive plugin.

Plugin: Archive
---------------

New features since the last beta plugin:

* Support for multiple compression strategies. (Snappy, LZ4, Gzip, None)
