================
Tjeksum (SHA256)
================

En tjeksum er en (næsten) unik alfanumerisk kode, genereret på baggrund af den
bit-vise indhold af en fil.

Det kan være en god idé at tjekke tjeksummen af en fil man har hentet over en
usikret forbindelse (f.eks. http frem for https), eller fra en ellers
upålidelig internetkilde. Således kan man være mere sikker på at hvad man har
hentet, faktisk er den ønskede fil. (Antaget, at man ellers har en sikker måde
at få fat i den forventede tjeksum på.)

Der findes en række forskellige tjeksum-algoritmer, hvor nok den mest populær
nutildags er SHA256.

På en Linux- eller OS X-maskine kan bruge kommandolinjeværktøjet ``sha256sum``
til at beregne SHA256-summen af en fil ved stien ``<fil-sti>``:

.. code-block:: shell

  $ sha256sum <fil-sti>

På en Windows-maskine, kan man til gengæld bruge kommandolinjeværktøjet
``certUtil``:

.. code-block:: bat

  > certUtil -hashfile <fil-sti> SHA256
