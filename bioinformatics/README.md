# List of bioinformatic resources of the Bleeker Lab
Here is a list of resources we developed during the course of our work of through collaborations. 

# Genseq 
This is the "supercomputer" that you can use to perform heavy duty jobs such as read alignment to a genome etc. 
It is composed of a headnode (*h0*) and four computing nodes (*cn00* to *cn04*).  

It is nicknamed **genseq** and is maintained by the team of Timo Breit. Please contact [Wim de Leeuw](https://www.uva.nl/profiel/l/e/w.c.deleeuw/w.c.deleeuw.html) (system administrator) to get access. 

## Accessing genseq
There is no graphical user interface to genseq. Instead, you will need to use the Shell.   
To connect, type in your favorite Shell the following commands:
* `ssh -X -Y genseq-h0.science.uva.nl` if you want to access the head node and start some text editor (type `gedit` once logged in).
* `ssh genseq-cn[00, 01, 02 or 03].science.uva.nl` to connect to one of the computing node.  

To get an understanding of the Shell and make use of it, please follow this tutorial to get some basic knowledge: https://swcarpentry.github.io/shell-novice/  

## Genome references (fasta format)
The fasta files of the different genomes (both public and private) are available from the Zenodo archive: https://doi.org/10.5281/zenodo.3613695

* Solanum lycopersicum (assemblies 3.0 and 4.0):
  * S_lycopersicum_chromosomes.3.00.fa.tar.gz
  * S_lycopersicum_chromosomes.4.00.fa.tar.gz
* Solanum pennellii (one version only from Bolger et al., 2014) : Spenn.fasta.tar.gz
* Solanum habrochaites LA1777 (technology hotel project 2018): LA1777.final.fasta  
* Solanum habrochaites PI127826 (technology hotel project 2018): PI127826.final.fasta  
* Solanum habrochaites LYC4 (from the paper of Aflitos et al. 2014. 3rd assembly version). S_habrochaites_LYC4...
  
## Genome browsers
You will need a user name and a password. Please contact your local genome browser admin: m.galland@uva.nl 

### Solanum lycopersicum ITAG3.0
Genome browser based on the ITAG3.0 genome assembly. 
Contains a wealth of information related to wild tomato species mRNA-Seq, sRNA-Seq and PARE-Seq.
Link (password protected): http://genseq-h0.science.uva.nl/MarcsJBrowse/?data=ITAG3.0

### Solanum pennellii 
Link (password protected) :http://genseq-h0.science.uva.nl/MarcsJBrowse/?data=Spen

## Blast server (Sequence Server) for tomato genomics

The following link redirects to a Sequence Server implementation that allows you to perform BLAST on custom resources: http://genseq-h0.science.uva.nl/SeqServ/

Available resources:
- 19 Trinity-assembled de novo transcriptomes of wild tomato genotypes.  
- Two *S. habrochaites* genomes assembled through 10X Linked reads and Optical Mapping: LA1777 and PI127826.


## Online Shiny applications

Gene expression visualisation (mRNA-Seq, 20 wild genotypes).    
https://bleekerlab.shinyapps.io/rnaseqvis/
