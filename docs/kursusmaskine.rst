=============
Kursusmaskine
=============

Det kan være praktisk at give underviserne og instruktorerne en maskine til
brug i undervisning. F.eks. til hurtig upload af delte filer.

``public_html``
---------------

Det er ikke usædvanligt for brugere på en Unix maskine at eksponere en given
mappe under deres hjemmemappe bag et URL som ``<hostname>/~<username>/``.
F.eks. `onlineta.org/~oleks/ <https://onlineta.org/~oleks/>`_.

Konventionen er at det er mappen ``~/public_html/`` (relativt til den hhv.
Unix-bruger) der blicer således eksponeret, hvis sådan en findes.

Følgende Nginx-konfiguration ruller denne funktionalitet ud til Unix-brugere på
maskinen:

.. code-block:: nginx

  location ~ "^/~(.*?)(/.*?)?$" {
    alias /home/$1/public_html/$2;
    autoindex on;
  }

``hidden_html``
---------------

Konfigurationen for ``public_html`` for oven, har indeksering slået til. Det
vil sige at hvis den givne sti referer til en mappe, da vises mappens indhold.
Det er nogen gange et uønsket funktionalitet, f.eks. hvis man ønsker at dele
skjulte filer.

En konvention man kan tage i brug er at eksponere mappen ``~/hidden_html/``, i
stil med ``~/public_html/`` for oven, bag et URL som
``<hostname>/@<username/``, og så lade være med at slå indeksering til.

Følgende Nginx-konfiguration ruller denne funktionalitet ud til Unix-brugere på
maskinen:

.. code-block:: nginx

  location ~ "^/@(.*?)(/.*?)?$" {
    alias /home/$1/hidden_html/$2;
  }
