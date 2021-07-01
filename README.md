# Rhino-pipeline

Dry-lab archive for the Rhinoceros project

The Black rhinoceros is a native rhinoceros species in the fields of Africa, living throughout east, south and middle Africa. This species faces a large threat in the form of its own intestines and gut bacteria. Environment is a large contributor to this, diets vary greatly and gut bacteria form in different amounts. In order to determine the difference between wild and captive rhino’s gut microbiota, feces samples are therefore compared. Various tools can be used here to dissect the results. To optimize the data processing of the rhinoceros feces the Linux environment was used  with the help of the ONTrack, Kraken2 and Krona tools. ONTrack was used in order to process most of the data and achieve an accurate Consensus. Kraken2 Identifies the species from the consensus files which were created by the ONTrack pipeline, from this the  data visualization is created using Krona.  
This study was initiated in order to investigate if a pipeline could be created which could process these datafiles, with the use of ONTrack, Kraken2 and Krona this was achieved. With these tools the feces data from the black rhinoceros could be analyzed and processed. Through this analysis a better understanding should be achieved of the gut microbiome the rhinoceros has. This review also provides processed data from example datasets and show the different species found in this sample. 

**The Goal**

The goal of this project is to build a final pipeline based on the ONTrack that will be able to analyze the data that is obtained through metabarcoding on faeces. 

# Flowchart


![Flowchart BI V6 (1)](https://user-images.githubusercontent.com/80203184/122371937-8def1c80-cf60-11eb-8b15-9c78912c149a.png)

# Method
The workings of the rhino pipeline use a variation of tool to achieve a species identification and visualizations

**Nanoplot**

Nanoplot is a tool for long read sequencing data and alignments. Nanoplot produces informative QC graphs which display multiple aspects of sequencing data and accept input data in fastq or fasta format. These graphs containg length histograms, cumulative yied plots, violin plots of read length and quality over time. Nanoplot starts with a usage command:

`NanoPlot [-h] [-v] [-t THREADS] [--verbose] [--store] [--raw]`

This command allows the user to create a statistical summary, a number of plots and a html summary file. The tool further allows adaptation to the users wishes, allowing variation in different parameters.

The Nanoplot files and installation can be found at https://github.com/wdecoster/NanoPlot
**ONTrack**

The ONTRack pipeline is a rapid and accurate barcoding pipeline for tracking species biodiversity on site. The pipeline allows for a meta-barcoding analysis, with this script it is possible to achieve a more accurate consensus sequence. The **MetatONTrack.sh** script produces what the EPI2ME 16S workflow does, it blasts each read against an NCBI-downloaded database and afterwards it saves sets of the reads matchint the different species to seperate files. After this the **ONTrack.R** script is run to obtain a accurate consensus sequence. 

The ONTRack files and installation can be found at: https://github.com/MaestSi/ONTrack

**Kraken2**

Kraken2 is a taxonomic sequence classifier that assigns taxonomic labels to DNA sequences. Kraken examines the K-mers within a query sequence and uses the information within those K-mers to query a database. In order to classify a set of sequences use the following command from Kraken2:
`kraken2 --db database filename --output filename.kraken --report filename.kraken.report`

The output of this will be send to a standard output by default. Files containing the sequences that are to be classified should be specified on the command line. 

The Kraken2 files and installation can be found at: https://github.com/DerrickWood/kraken2

**Krona**
Krona is a visualization tool that allows a new intuitive way to view relative abundances and confidences within a complex system of metagenomic classifications. Krona creates an interactive polar coordinated zooming which allows individual identifications to be more visually expressed, it does this in combination with coloring to distinguish itself. 

The Krona files and installation can be found at: https://github.com/marbl/Krona

# Data

Before the implementation of the Pipeline a quality check took place using the Nanoplot which visualized the data quality and created a html summary file. Under **NanoPlot-report.html** a statistical summary can be found where the mean read quality is available.

The ONTrack pipeline was implemented 


# Citations

Wouter De Coster, Svenn D’Hert, Darrin T Schultz, Marc Cruts, Christine Van Broeckhoven, NanoPack: visualizing and processing long-read sequencing data, Bioinformatics, Volume 34, Issue 15, 01 August 2018, Pages 2666–2669, https://doi.org/10.1093/bioinformatics/bty149

Maestri S, Cosentino E, Paterno M, Freitag H, Garces JM, Marcolungo L, Alfano M, Njunjić I, Schilthuizen M, Slik F, Menegon M, Rossato M, Delledonne M. A Rapid and Accurate MinION-Based Workflow for Tracking Species Biodiversity in the Field. Genes. 2019; 10(6):468.

Wood, D.E., Lu, J. & Langmead, B. Improved metagenomic analysis with Kraken 2. Genome Biol 20, 257 (2019). https://doi.org/10.1186/s13059-019-1891-0

Ondov BD, Bergman NH, and Phillippy AM. Interactive metagenomic visualization in a Web browser. BMC Bioinformatics. 2011 Sep 30; 12(1):385.




