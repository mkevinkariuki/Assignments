## 1. Download sequence from NCBI
* Download sequnces - Accession number: SRR24415235  
* Confirm the sequenceing platform used 

## 2.Unzip downloaded sequence 
* gunzip SRR24415235.fastq.gz 

## 3. Check quality of the sequence 
* if fastqc environment not available ; create environment
* if environment is available ; conda activate environment 

* solution: conda activate qc environment 
* fastqc SRR24415235.fastq.gz

* attach report: RR24415235_fastqc.html

## 4. Bacterial assembly 
* conda activate flye 
* flye --nano-raw SRR24415235.fastq -t 20 -o assembly_tutorial
* Results:  
  Total length:	5227295  
	Fragments:	3  
	Fragments N50:	5055639  
	Largest frg:	5055639  
	Scaffolds:	0  
	Mean coverage:	116  



## 5. Visualize the assembly graph
* ls assembly_tutorial/
* cd assembly_tutorial/
* bandage load assembly_graph.gfa
