=======
Maskine
=======

En generisk maskineopsætning.

Det er en god idé at følge vejledningen `My First 5 Minutes On A Server; Or,
Essential Security for Linux Servers
<https://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers>`_.
Den er gammel, men stadig højst relevant.

Mosh
----

`Mosh <https://mosh.org/>`_ er en UDP-baseret erstatning for SSH. Den er
generelt meget mere behagelig at bruge end SSH i denne trådløse verden.

Den er nem nok at installere på en Debian::

    apt-get install mosh

Men bruger man et firewall (som man jo bør), skal man lige åbne op for de
relevante UDP-porte.

F.eks., hvis man bruger ufw::

    ufw allow 60000:61000/udp
