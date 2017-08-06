.. vim: spell spelllang=da

==============
``dikunix.dk``
==============

``dikunix.dk`` kører på en VPS fra transip_, og har OpenBSD_ som styresystem.

.. _transip: https://www.transip.eu
.. _OpenBSD: https://www.openbsd.org

------------
Spindelnisse
------------

``dikunix.dk`` bruger |httpd|_ som spindelnisse.

Konfiguration foregår i ``/etc/httpd.conf`` (se også |httpd.conf|_).

Kør ``httpd -n`` for at validere konfigurationen før du rør ved nissen.

Selve nissen styres vha. |rc.d|_. F.eks., for at for at genstarte nissen kør
følgende:

.. code-block:: shell

  $ /etc/rc.d/httpd restart

Hvis det går galt, kan du tjekke halen af ``/var/log/daemon``.

.. |httpd| replace:: ``httpd(8)``
.. _httpd: https://man.openbsd.org/httpd

.. |httpd.conf| replace:: ``httpd.conf(5)``
.. _httpd.conf: https://man.openbsd.org/httpd.conf

.. |rc.d| replace:: ``rc.d(8)``
.. _rc.d: https://man.openbsd.org/rc.d
