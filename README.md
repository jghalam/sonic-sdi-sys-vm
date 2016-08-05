sonic-sdi-sys-vm
-------------
SDI VM -  System Device Interface for VM

Description
-----------
SDI-VM presents an abstraction of the hardware (thermal sensors, fans, LEDs,
optics, etc.) in a VM environment. SDI-VM's sole client is PAS and it queries
the devices using the API defined in sdi-api.

Building
--------
Please see the instructions in the sonic-nas-manifest repo for more details on the common build tools.  [Sonic-nas-manifest](https://stash.force10networks.com/projects/SONIC/repos/sonic-nas-manifest/browse)

Development Dependencies:

 - sonic-logging
 - sonic-common-utils
 - sonic-sdi-api
 - sonic-db-sql

Dependent Packages:

 - libsonic-logging1 libsonic-logging-dev libsonic-common1 libsonic-common-dev sonic-sdi-api-dev

BUILD CMD: sonic_build --dpkg libsonic-logging1 libsonic-logging-dev libsonic-common1 libsonic-common-dev sonic-sdi-api-dev libsonic-db-sql1 libsonic-db-sql-dev -- clean binary

(c) Dell 2016
