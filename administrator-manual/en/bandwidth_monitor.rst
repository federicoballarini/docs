.. _ntopng-section:

=================
Bandwidth monitor
=================

**Bandwidth monitor** module allows you to analyze real-time network traffic using 
`ntopng <https://www.ntop.org/products/traffic-analysis/ntop/>`_ under the hood.
**ntopng** is a powerful tool that evaluates the bandwidth used by
individual hosts and identifies the most commonly used network protocols.


Dashboard
=========

:guilabel:`Dashboard` page provides an overview on network usage displaying traffic information on some graphical widgets.


Status
------

:guilabel:`Status` section informs you whether bandwidth monitor is currently enabled and provides :guilabel:`Open bandwidth monitor app`
button to access **ntopng** web interface.


Top local hosts
---------------

This table shows the list of hosts belonging to local networks that are currently generating most throughput,
either downloading or uploading.
This widget can help identify any hosts that are using a lot of bandwidth.


Top remote hosts
----------------

This table shows the list of remote hosts that are currently generating most throughput, either downloading
or uploading.


Traffic by interface
--------------------

This chart plots the throughput generated by monitored interfaces during the last 5 minutes.


Traffic by protocol
-------------------

This chart plots the traffic divided by protocol during the last 5 minutes. **ntopng** tries to recognize
various layer 7 protocols such as HTTP, TLS, DNS, SIP, Facebook, Spotify, Zoom, etc.


Settings
========

In :guilabel:`Settings` page you can manage **Bandwidth monitor** configuration through the following controls:

* :guilabel:`Enable bandwidth monitor`: if enabled, all traffic passing through selected network interfaces
  will be analyzed. Depending on the capabilities of your server, it may cause a slowdown of 
  the network and an increase in system load.
* :guilabel:`Interfaces`: the network interfaces **ntopng** will listen to.
* :guilabel:`Web interface port`: the TCP port where **ntopng** web interface should be available.
  By default TCP port is **3000** and can be accessed from green zone.
* :guilabel:`Enable authentication`: if enabled, **ntopng** web interface will require login credentials.
  Username is ``admin`` and default password is ``admin``.

When **Bandwidth monitor** is enabled, **ntopng** web interface is available at: ``http://<SERVER_NAME>:<WEB_INTERFACE_PORT>``.
A link to **ntopng** web interface is provided in :guilabel:`Dashboard` and :guilabel:`Settings` pages.


Logs
====

In :guilabel:`Logs` page you can examine systemd journal of **ntopng** unit.
