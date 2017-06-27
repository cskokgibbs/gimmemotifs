.. _`simple_examples`:

Simple examples
===============

Install a genome
----------------

Any genome on UCSC can be installed automatically using ``gimme genome``.

Install the hg38 genome in the directory ``~/genomes``:

::

    $ gimme genome ~/genomes/ hg38


Install the mm10 genome in the directory ``/data/genomes``:

::

    $ gimme genome /data/genomes mm10


Predict de novo motifs
----------------------

For a quick analysis, to see if it works:

::
    
    $ gimme motifs TAp73alpha.bed -g hg19 -n gimme.p73 -a small -t Homer,MDmodule,BioProspector

For a full analysis:

::
    
    $ gimme motifs TAp73alpha.bed -g hg19 -n gimme.p73 


Open the file ``gimme.p73/motif_report.html`` in your web browser to see the results.

Compare motifs between data sets
--------------------------------

::

    $ gimme maelstrom hg19.blood.most_variable.1k.txt hg19 maelstrom.out/

Create sequence logos
---------------------

::

    $ gimme logo -i p53_Average_8

This will generate ``p53_Avarage_8.png``.

.. image:: images/p53_Average_8.png

Use the ``-p`` argument for a different pwm file. 
The following command will generate a logo for every motif in ``custom.pwm``.

::  

   $ gimme logo -p custom.pwm

 