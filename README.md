# lab-genom-comp
questa è la repository del corso :)
# titoli: Kmer based survey

 ` ` ` bash
 # comando per fare il quality control delle raw sequenziate (1)
 /home/PERSONALE/mirko.martini3/Lab_CompGeno/00_practice/00_data/00_reads/SRR11672503_1.fastq.gz
 
` ` ` bash
# comando per fare il quality control delle raw sequenziate (2)
/home/PERSONALE/mirko.martini3/Lab_CompGeno/00_practice/00_data/00_reads/SRR11672503_2.fastq.gz

` ` ` phyton 
# Trim reads in a sliding window approach
trimmomatic PE -threads 20 -phred33 SRR11672503_1.fastq.gz SRR11672503_2.fastq.gz SRR11672503_1_paired.fastq SRR11672503_1_unpaired.fastq SRR11672503_2_paired.fastq SRR11672503_2_unpaired.fastq ILLUMINACLIP:/opt/miniforge3/envs/assembly/share/trimmomatic-0.40-0/adapters/TruSeq3-PE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36 2> stats_trimmomatic.log
