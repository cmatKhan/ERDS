# A note about this fork

The authors of the source of this fork have not made a release for their software 
on github. Instead, they keep one directory called erds1.1 and another called 
erds_tcag with a note in the main README that tcag is a reimplementation (See below).

All I have done is removed erds_tcag from v1.1, and made a formal release of v1.1, and then 
merged a branch with erds_tcag into the main branch, deleted erds1.1, and called that 
v2.0.

To reiterate: v2.0 is exactly the same as erds_tcag in the source of this fork on 20221004.

# ERDS

ERDS is designed for detection of copy number variants (CNVs) on human genomes from next generation sequence data, utilizing information from read depth of short reads and SNV heterozygosity.

The original version can be found from subdirectory named "erds1.1".

Brett Trost and Joe Whitney (The Centre for Applied Genomics (TCAG), Hospital for Sick Children, Toronto) improved memory usage and performance of ERDS and their team published a paper describing a workflow for detecting CNVs from WGS data (The American Journal of Human Genetics 102.1 (2018): 142-155). The modifed code version can be found from subdirectory named "erds_tcag". A simple compilation step is required - just run "make" within the "src" directory.

In addition to memory and peformance improvements, the TCAG version of ERDS also contains a modification that affects the output of ERDS when the median insert size of the DNA library is small. Please see the above paper (specifically Figure S22 in the supplementary materials) for further details. Please note that for the TCAG version of ERDS, you must add the directory containing samtools to your PATH environment variable.

### Citation

If you use ERDS for publication, please cite:

Zhu M, Need AC, Han Y, Ge D, Maia JM, Zhu Q, Heinzen EL, Cirulli ET, Pelak K, He M, Ruzzo EK, Gumbs CE, Singh A, Feng S, Shianna KV and Goldstein DB. Using ERDS to Infer Copy-Number Variants in High-Coverage Genomes. The American Journal of Human Genetics. Volume 91, Issue 3, 7 September 2012, Pages 408-421.
