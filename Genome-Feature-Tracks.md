###Canonical Feature Tracks

Gene
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_gene.gff   

Exons
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_exon.gff   

Intron
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_intron.gff   

Promoter (= 1kbp 5' of genes)
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_1k5p_gene_promoter.gff   

Transposable Elements
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_TE.gff   

Complement to Gene, Promoter, and TE tracks
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_COMP_gene_prom_TE.bed   

All CGs
http://eagle.fish.washington.edu/trilobite/Crassostrea_gigas_v9_tracks/Cgigas_v9_CG.gff

_Complete details regarding the development of these tracks can be found in [this IPython Notebook](http://nbviewer.ipython.org/github/sr320/ipython_nb/blob/master/TJGR_OysterGenome_IGV.ipynb) as well as in this [methods section](https://peerj.com/articles/215/#p-7).


***

###Crassostrea gigas high-throughput bisulfite sequencing (gill tissue)
Citation: Gavery, Mackenzie; Roberts, Steven (2013): Crassostrea gigas high-throughput bisulfite sequencing (gill tissue). figshare. 
<http://dx.doi.org/10.6084/m9.figshare.749728>


This fileset contains genomic feature tracks from methylation-enriched high-throughput bisulfite sequencing and RNA-seq analysis for Pacific oyster (Crassostrea gigas) gill tissue. Feature tracks were developed to be viewed with Integrative Genomics Viewer (http://www.broadinstitute.org/igv/) in conjunction with the C. gigas genome (Fang et al. 2012). All data and instructions are also available at <http://oystergen.es/bigill>.

File descriptions:    
[BiGill_CpG_methylation.igv](http://files.figshare.com/1252773/BiGill_CpG_methylation.igv) - Location and proportion of methylation for all analyzed CpG dinucleotides with greater than 5x coverage.    

[BiGill_exon_clc_rpkm.igv](http://files.figshare.com/1252772/BiGill_exon_clc_rpkm.igv) - Exon-specific gene expression values (RPKM) from RNA-seq analysis.    

[BiGill_igv_charlie.xml](http://files.figshare.com/1252770/BiGill_igv_charlie.xml) - A session file, which loads methylation and RNA-seq feature tracks as well as the location of C.gigas genome features.   

[Query to derive_CG_AllData_IGV.txt](http://files.figshare.com/1252771/Query_to_derive_CG_AllData_IGV.txt) - Query (SQLShare) used to derive the methylation feature track from the original methratio output (http://goo.gl/5LGq9Q)