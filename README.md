# share-seq
Creat a Docker environment to analyze share-seq data. Using pipeline released by Ma et al. (https://github.com/masai1116/SHARE-seq-alignment)\
https://hub.docker.com/r/jiangyanyu/shareseq
PRETTY_NAME="Debian GNU/Linux 10 (buster)"


Installed packages:

GNU parallel 20161222, bcl2fastq v2.20.0.422, fastp version 0.12.4, zcat (gzip) 1.9, STAR version=2.7.7a, bin/bowtie2-align-s version 2.2.5, Python 2.7.16, UMI-tools version: 1.1.1, samtools 1.11, openjdk 11.0.12 (https://github.com/nextcloud/docker/issues/380, https://tecadmin.net/install-java-8-on-debian/), picard 2.14.1, R version 3.5.2 (2018-12-20) -- "Eggshell Igloo", featureCounts Version 2.0.1, read_distribution.py 4.0.0, bedtools v2.27.1

Download and transfer gtf and index files to corresponding folders in container.

1) Run with bash ./xxx.sh
2) create conda python2.7 environment, install Bio, levenshtein, optparse (not working), yaml (needs pyyaml), pysam
3) in the .sh file, activate conda py2 environment at the beginning. deactivate at the end of the script.
4) python3.8 will give errors due to encode and decode between byte and string, dic etc
5) STAR index files
  a) use cellranger to get reference genome and gtf files (cellranger_mm10_ref_v2020-A.sh)
  b) use STAR to build reference index (499df463a285:/home/10x/mm10# STAR --runThreadN 20 --runMode genomeGenerate  --genomeFastaFiles ./fasta/genome.fa --sjdbGTFfile ./genes/genes.gtf)
6) 
7) 
  


