.. _webui:

Web UI
======

Tutor comes with a web user interface (UI) that allows you to administer your Open edX platform remotely. It's especially convenient for remote administration of the platform.

Launching the web UI
--------------------

::

    tutor webui start

You can then access the interface at http://localhost:3737, or http://youserverurl:3737. 

.. image:: img/webui.png

All ``tutor`` commands can be executed from this web UI: you just don't need to prefix the commands with ``tutor``. For instance, to deploy a local Open edX instance, run::

    local quickstart

instead of ``tutor local quickstart``.

Authentication
--------------

**WARNING** Once you launch the web UI, it is accessible by everyone, which means that your Open edX platform is at risk. If you are planning to leave the web UI up for a long time, you should setup a user and password for authentication::

    tutor webui configure
