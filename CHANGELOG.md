## 4.1.5 2020-01-11 <dave at tiredofit dot ca>

   ### Changed
      - Additional fix for check_service_initialized function to properly look for finished /etc/s6/services processes

## 4.1.4 2020-01-11 <dave at tiredofit dot ca>

   ### Changed
      - Fix for check_service_initialized function to properly look for finished /etc/s6/services processes

## 4.1.3 2020-01-10 <dave at tiredofit dot ca>

   ### Changed
      - Remove code showing $dirname erronously on process startup

## 4.1.2 2020-01-10 <dave at tiredofit dot ca>

   ### Added
      - Quiet down sudo error
      - Zabbix 4.4.4 Agent


## 4.1.1 2020-01-02 <dave at tiredofit dot ca>

   ### Changed
      - check_service_initialized was throwing false information


## 4.1.0 2020-01-01 <dave at tiredofit dot ca>

   ### Added
      - Start splitting out Defaults into seperate /assets/functions/* files

   ### Changed
      - Cleanup of Permissions Changing routines

## 4.0.1 2020-01-01 <dave at tiredofit dot ca>

   ### Added   
      - New text output for Notices

   ### Changed
      - Additional checks to ensure cont-init.d scripts have finished executing

## 4.0.0 2020-01-01 <dave at tiredofit dot ca>

   ### Added
      - Now relying on Container Level functions file
      - Easier methods for displaying console output 
      - Colorized Prompts 
      - Cleaner Startup Routines
      - Sanity Check to not start any processes until all startup scripts completed
    
    ### Changed
      - When DEBUG_MODE set stop taking over SMTP functionality. Require DEBUG_SMTP=TRUE instead

## 3.14.0 2019-12-15 <dave at tiredofit dot ca>

   ### Changed
      - Change the way S6 Overlay is installed


## 3.13.0 2019-11-27 <dave at tiredofit dot ca>

   ### Changed
      - Change Zabbix Agent from 4.2.x to 4.4.x release


## 3.12.0 2019-11-27 <dave at tiredofit dot ca>

   ### Changed
      - Change Zabbix Agent Version from 4.2.x to 4.4.x

   ### Reverted


## 3.11.0 2019-11-27 <dave at tiredofit dot ca>

   ### Added
      - Add env var SMTP_TLSTRUSTFILE (optional)

## 3.10 2019-08-29 <edisonlee at selfdesign dot org>

* Move S6 Overlay to default variables.

## 3.9 2019-07-23 <dave at tiredofit dot ca>

* Fix for S6 Overlay bulldozing over /bin

## 3.8 2019-04-26 <dave at tiredofit dot ca>

* Buster stable version

## 3.7 2019-04-26 <dave at tiredofit dot ca>
	
* Update Zabbix to 4.2

## 3.6.1 2019-04-06 <dave at tiredofit dot ca>

* S6 Overlay 1.22.1.0

## 3.6 2018-10-17 <dave at tiredofit dot ca>

* Force executible permissions on S6 Directories

## 3.5 2018-10-14 <dave at tiredofit dot ca>

* Update Zabbix to 4.0 Branch

## 3.4 2018-08-15 <dave at tiredofit dot ca>

* Update MSMTP

## 3.3 2018-07-02 <dave at tiredofit dot ca>

* Add Sudo

## 3.3 2018-07-02 <dave at tiredofit dot ca>

* Revert back to using && \ instead of ; \ in Dockerfile
* Add ENABLE_GMAIL_SMTP environment variable thanks to @joeyberkovitz

## 3.2 2018-04-22 <dave at tiredofit dot ca>

* Update 01-permissions to quiet down if no UIDs changed.
* Refinements to MailHog, to always route through msmtp

## 3.1 2018-03-25 <dave at tiredofit dot ca>

* Update MailHog Test Server Startup

## 3.0 2018-03-14 <lesliesit at outlook dot com>

* Add 01-permissions script to support change uid & gid and add user to group:
* USER_<USERNAME>=<aNewNumber>
* GROUP_<GROUPNAME>=<aNewNumber>
* GROUP_ADD_<USERNAME>=<aGroupName>
* UID & GID in /etc/passwd & /etc/group will be modified.
* Old 01- 02- 03- scripts renamed after the new 01-permissions as 02- 03- 04-

## 2.11 2018-02-17 <dave at tiredofit dot ca>

* Update Permissions for Logrotate

## 2.10 2018-01-30 <dave at tiredofit dot ca>

* Add Zabbix Updated Package Check
* Update S6 Overlay 1.21.1.2

## 2.9 2017-12-24 <dave at tiredofit dot ca>

* Add custom crontab importing from /assets/cron-custom/

## 2.8 2017-10-23 <dave at tiredofit dot ca>

* Update S6 Overlay to 1.21.1.1

## 2.7.3 2017-09-30 <dave at tiredofit dot ca>

* Revert from `slim` variants

## 2.7.2 2017-09-30 <dave at tiredofit dot ca>

* Remove requirement to use wget 
* Minor S6 Overlay tweak for Stretch

## 2.7.1 2017-09-27 <dave at tiredofit dot ca>

* Tamed verbosity

## 2.7 2017-09-26 <dave at tiredofit dot ca>

* Made Service Enabling/Disabling more Verbose
* Switched to -slim Variants

## 2.6 2017-09-17 <dave at tiredofit dot ca>

* Fix some scripting errors

## 2.5 2017-09-01 <dave at tiredofit dot ca>

* Update S6 overlay to 1.20.0.0

## 2.4 2017-08-28 <dave at tiredofit dot ca>

* Added Debian Stretch and Wheezy 
* Added Official Zabbix Agent 3.4 instead of compiling from source

## 2.3 2017-08-28 <dave at tiredofit dot ca>

* Added `DEBUG_SMTP` environment variable to trap SMTP messages accesible via port 8025

## 2.2 2017-08-27 <dave at tiredofit dot ca>

* Added MSMTP to be able to route mail to external hosts

## 2.1 2017-08-27 <dave at tiredofit dot ca>

* Added DEBUG_MODE environment variable
* Added TIMEZONE environment variable
* Added ENABLE_CRON, ENABLE_ZABBIX switches
* Built mechanisms to not start processes until container initialized
* Zabbix Agent Configuration can be controlled and adjusted via Environment Variables
* General Tidying Up
