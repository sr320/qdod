qdod: Querying Disparate Oyster Datasets
====

This respository provides access to genomic data and workflows (IPython notebooks) that are being integrated as part of effort to increase effeciency of biological discovery. During the initial phases the focus is on the Pacific oyster and primary data from the [Roberts Lab](http://faculty.washington.edu/sr320).


##Raw Data

#### Select Genomic Data

| ID                      | Platform | Molecule | Tissue | Length | Files                                                                                                         |
|-------------------------|----------|---------------|------------------|-------------|------------------------------------------------------------------------------------------------------------------|
| BB3                     | SOLiD    | RNA           | gill             | 25 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_BB3.csfasta); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_BB3.qual)                 |
| DH3                     | SOLiD    | RNA           | gill             | 25 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_DH3.csfasta); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_DH3.qual)                 |
| DH2                     | SOLiD    | RNA           | gill             | 25 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_DH2.csfasta); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_DH2.qual)                 |
| GE                      | SOLiD    | RNA           | larvae           | 50 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_RbbertsLab_GE_F3_QV.qual); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20091105_RbbertsLab_GE_F3.csfasta)           |            
| GC                      | SOLiD    | RNA           | larvae           | 50 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20100107_Roberts_GC_F3_QV.qual); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20100107_Roberts_GC_F3.csfasta)    |
| SBunmeth                | SOLiD    | DNA           | gill             | 25 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20110412_SB_UNMETH.csfasta); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20110412_SB_UNMETH.qual)           |
| SBmeth                  | SOLiD    | DNA           | gill             | 25 x 1      | [csfasta](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20110412_SB_METH.csfasta); [qual](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/solid0078_20110412_SB_METH.qual)             |
| BSseqGill               | Illumina | DNA           | gill             | 36 x 1      | [fastq](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/filtered_BSseqGill_L003_R1.fastq)            |
| ETStagseq               | Illumina | RNA           | gill             |             | [zip](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/ETS_tagseq.zip)                              |
| BiGosperm               | Illumina | DNA           | sperm            | 72 x 2      | [fastq1](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/filtered_174gm_A_NoIndex_L006_R1.fastq); [fastq2](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/filtered_174gm_A_NoIndex_L006_R2.fastq)      |
| BiGillRNA               | Illumina | RNA           | gill             | 50 x 2      | [fastq1](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/BiGillRNA_GACTAAGA_1.fastq); [fastq2](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/BiGillRNA_GACTAAGA_2.fastq) 
| BiGoRNA                 | Illumina | RNA           | sperm            | 50 x 2      | [fastq1](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/BiGillRNA_GACTAAGA_1.fastq); [fastq2](http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_HTSdata/BiGillRNA_GACTAAGA_2.fastq) 

---

#### Select Genomic Data in NCBI
[NCBI SRA] [_Crassostrea gigas_ MBD bisulfite sequencing – gill](http://www.ncbi.nlm.nih.gov/sra/SRX327373)   [NCBI SRA] [*Crassostrea gigas* RNA-seq – gill](http://www.ncbi.nlm.nih.gov/sra/SRX367081)   [NCBI SRA] [*Crassostrea gigas* RNA-seq – male gonad](http://www.ncbi.nlm.nih.gov/sra/SRX3903468)   [NCBI SRA] [*Crassostrea gigas* bisulfite sequencing – male gonad](http://www.ncbi.nlm.nih.gov/sra/SRX386228)  
---
#### Select Genomic Feature Tracks
 

