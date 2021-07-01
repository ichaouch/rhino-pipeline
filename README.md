# rhino-pipeline

Dry-lab archive for the Rhinoceros project

The Black rhinoceros is a native rhinoceros species in the fields of Africa, living throughout east, south and middle Africa. This species faces a large threat in the form of its own intestines and gut bacteria. Environment is a large contributor to this, diets vary greatly and gut bacteria form in different amounts. In order to determine the difference between wild and captive rhino’s gut microbiota, feces samples are therefore compared. Various tools can be used here to dissect the results. To optimize the data processing of the rhinoceros feces the Linux environment was used  with the help of the ONTrack, Kraken2 and Krona tools. ONTrack was used in order to process most of the data and achieve an accurate Consensus. Kraken2 Identifies the species from the consensus files which were created by the ONTrack pipeline, from this the  data visualization is created using Krona.  
This study was initiated in order to investigate if a pipeline could be created which could process these datafiles, with the use of ONTrack, Kraken2 and Krona this was achieved. With these tools the feces data from the black rhinoceros could be analyzed and processed. Through this analysis a better understanding should be achieved of the gut microbiome the rhinoceros has. This review also provides processed data from example datasets and show the different species found in this sample. 

**The Goal**

The goal of this project is to build a final pipeline based on the ONTrack that will be able to analyze the data that is obtained through metabarcoding on faeces. 

flowchart:


![Flowchart BI V6 (1)](https://user-images.githubusercontent.com/80203184/122371937-8def1c80-cf60-11eb-8b15-9c78912c149a.png)


Follow the installation steps from these 3 githubs:

https://github.com/MaestSi/ONTrack

https://github.com/DerrickWood/kraken2

https://github.com/marbl/Krona/tree/master/KronaTools




