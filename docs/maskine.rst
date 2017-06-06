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
relevante UDP-porte. Mosh vil starte med at optage port 60000 og 60001, og
ellers inkrementere port-nummeret efter flere samtidige forbindelser. Det
betyder at foventer man ikke mere end 9 forbindelser via Mosh ad gangen, kan
man nøjes med at åbne op for portene 60000 til 60010.

F.eks., hvis man bruger ufw::

    ufw allow 60000:60010/udp
