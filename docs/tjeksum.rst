=======
Tjeksum
=======

En tjeksum er en (næsten) unik alfanumerisk kode, genereret på baggrund af den
bit-vise indhold af en fil.

Det kan være en god idé at tjekke tjeksummen af en fil man henter over en
usikret forbindelse (f.eks. http frem for https), eller fra en ellers
upålidelig internettjenneste. Således kan du være mere sikker på at hvad du har
hentet faktisk er den fil du ønskede at hente.

På en Linux- eller OS X-maskine kan bruge kommando-linjeværktøjet ``sha256sum``:

.. code-block:: shell

  $ sha25sum <file>.ova

På en Windows-maskine, kan bruge kommando-linjeværktøjet ``certUtil``:

.. code-block:: bat

  > certUtil -hashfile <file>.ova SHA256
