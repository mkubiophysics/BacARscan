
# BacARscan

# Bacterial Antibiotic Resistance scan

# In-silico resource to discern diversity in antibiotic resistance genes

Created by the Computational Biology Lab at Department of Biophysics, University of Delhi South Campus

Developer: Deeksha Pandey (deeksha.pandey.biophysics@south.du.ac.in)

[Graphical_Abstarct]
(https://user-images.githubusercontent.com/43174322/174740309-19892e36-7004-40a7-aff1-7f9af309346a.png)

# Description
Bacterial Antibiotic Resistance scan (BacARscan) (http://proteininformatics.org/mkumar/bacarscan/) that can detect, predict and characterize ARGs in -omics datasets, including short sequencing, reads, and fragmented contigs. Benchmarking on an independent non-redundant data set revealed that the performance of BacARscan was better than other existing methods with ca. 92% precision and 95% F-measure on a combined dataset of ARG and nonARG proteins. One of the most notable improvements of BacARscan over other ARG annotation methods is its ability to work on genomes and small reads sequence libraries with equal efficiency and without any requirement for assembly of short reads. Thus, BacARscan can be helpful in monitoring the prevalence and diversity of ARGs in microbial populations and metagenomics samples from animal, human and environmental settings. 

# Dependencies
***********How to use it? **************

######Files description#####

nARGhmm: Library of 254 nucleotide ARG profile HMMs

pARGhmm: Library of 254 protein ARG profile HMMs
ARG_Annotations: Annotation of 254 ARG profile HMMs

HMMER download and install as standalone using link: http://hmmer.org/download.html

*****Scanning of protein sequences will perform using hmmscan*****

/hmmer-3.1b2-linux-intel-x86_64/src/hmmscan --cpu 4 -E 0.000001 --tblout abc.out pARGhmm protein.fasta


****Scanning of gene sequences will perform using nhmmscan******

/hmmer-3.1b2-linux-intel-x86_64/src/nhmmscan --cpu 4 -E 0.000001 --tblout abc.out nARGhmm gene.fasta


Using above commands user can scan their protein and nucleotide sequences; upon search it will give the similarity score and e-value. Depending on the scores user can select hits and retrieve their complete annotation using “ARG_Annotations” file.

# Model set description

The BacARscan contained 254 ARG models.

# Annotation description

The BacARscan models have been annotated with diffrent fileds:

Antibiotic Class: annotation at the class level describes the class of antibiotics to which this entry confers resistance (e.g. tetracyclines, betalactams)
Antimicrobial Spectrum: The antimicrobial spectrum of an antibiotic means the range of microorganisms it can kill or inhibit. Antibiotics can be divided into broad-spectrum antibiotics, extended-spectrum antibiotics and narrow-spectrum antibiotics based on their spectrum of activity.
Resistance Mechanism: annotation at the mechanism level describes the molecular function that confers resistance to a given antibiotic class (e.g. Class D betalactamases, efflux etc.)
AMR Family: annotation at the family level describes the gene or protein group under which this entry falls (e.g. OXA betalactamase, Small multidrug resistance (SMR) protein family)
ID: this option describes the name and ID of the BacARscan model, constructed from sequences and unique id of the HMM model.
AMR Function: this option describes the detailed functional infromation of the ARGs.
AMR Protein names: this option describes the name of the AR protein or gene (e.g. Multidrug transporter EmrE (Efflux-multidrug resistance protein EmrE) (Ethidium resistance protein) (Methyl viologen resistance protein C)
Annotations for all model sets can be visit our website for latest version, Executable versions, source code, profile HMMs, annotations, seed sequences and usage instructions can be downloaded from http://proteininformatics.org/mkumar/bacarscan/
