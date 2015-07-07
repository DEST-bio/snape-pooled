
*SNAPE-pooled* computes the probability distribution for the frequency of the
minor allele in a certain population, at a certain position in the genome.

For more information, you can read the
paper _SNP calling by sequencing pooled samples_
(Raineri E, Ferretti L, Esteve-Codina A, Nevado B, Heath S, Pérez-Enciso M.
, BMC Bioinformatics. 2012 Sep 20;13:239. doi: 10.1186/1471-2105-13-239) which explains the formulae used in it.

Also, have a look at the manual in .tex format. 

To create the executable, type

``
make snape-pooled
``

The input format is SAMTOOLS' pileup and a typical incantation goes as follows:
``
./snape-pooled -nchr 10 -theta 0.001 -D 0.1 -fold folded \
-priortype informative   < example.pileup
``
