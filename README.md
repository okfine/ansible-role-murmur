ansible-role-murmur [![Build Status](https://travis-ci.org/okfine/ansible-role-murmur.svg?branch=master)](https://travis-ci.org/okfine/ansible-role-murmur)
=========

Ansible role to install and configure murmur (Mumble server).

Requirements
------------

This role is designed for use on the Operating Systems listed below.

* Debian/Ubuntu

Role Variables
--------------

The ```murmur_ab_on``` variable will enable or disable the autoban feature.

	murmur_ab_on: true

If [autoban](http://wiki.mumble.info/wiki/Murmur.ini#autobanAttempts.2C_autobanTimeframe_and_autobanTime) is enabled, the following variables will control multiple aspects of the autoban behavior.

	murmur_ab_attempts: 3
	murmur_ab_timeframe: 120
	murmur_ab_bantime: 300

The ```murmur_sv_welcome``` variable sets the server [welcome text](http://wiki.mumble.info/wiki/Murmur.ini#welcometext). If no variable is defined, the default value is used.

	murmur_sv_welcome:

The ```murmur_sv_port``` variable sets the server [listening port](http://wiki.mumble.info/wiki/Murmur.ini#port). If no variable is defined, the default value is used.

	murmur_sv_port: 64738


The ```murmur_sv_password``` variable sets the [server password](http://wiki.mumble.info/wiki/Murmur.ini#serverpassword). If no variable is defined, the server will be publicly available.

	murmur_sv_password: password


The ```murmur_sv_maxusers``` variable sets the [user limit](http://wiki.mumble.info/wiki/Murmur.ini#users).

	murmur_sv_maxusers: 10


The following variables will set the SSL certificate that mumble-server utilizes. If these variables are not defined, mumble-server will utilize the default self-generated cert/key.

	murmur_sv_sslcert:
	murmur_sv_sslkey:

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-murmur }

License
-------

BSD / MIT

Author Information
------------------

[okfine](https://github.com/okfine)
