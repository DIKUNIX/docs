=============
Kursusmaskine
=============

Det kan være praktisk at give underviserne og instruktorerne en maskine til
brug i undervi

`public_html`
-------------

.. code-block:: nginx
  location ~ "^/~(.*?)(/.*?)?$" {
    alias /home/$1/public_html/$2;
    autoindex on;
  }
