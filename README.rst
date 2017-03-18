UCHIME chimera checker
======================

Progressively check for chimeric sequences in the style of UPARSE-OTU_.

.. _UPARSE-OTU: http://www.drive5.com/usearch/manual/uparseotu_algo.html

UPARSE-OTU reads in sequences from a database and classifies them as
(among other things) chimeric or not. The database is initialized with
the most abundant sequence. If the next-most-abundant sequence is not
classified as a match with an existing OTU or a chimera formed from
existing OTUs, it is added to the OTU database.

This script mimics this behavior by calling UPARSE-REF_ once per
sequence in the input. If the sequence is classified as "other",
then it is added to the OTU database used for classifying later
sequences. The results of each iteration of UPARSE-REF are output.

.. _UPARSE-REF: http://www.drive5.com/usearch/manual/uparseref_algo.html

Requirements
------------

This script calls usearch_, which must be installed and on your executable
path.

.. _usearch: http://www.drive5.com/usearch/

Author
------

Scott Olesen: `swo at alum.mit.edu`
