# How to upload NGS sequencing files to the EMBL-EBI European Nucleotide Archive
This protocol is helpful if you want to publish NGS datasets (part of Research Data Management). You will be able 


the public EMBL European Nucleotide Archive to get publish datasets (part of Research Data Management)
If you wonder how to archive fastq file sequencing or other datasets, here's a couple of way to do it.

The complete documentation of ENA (Guidelines and Tutorials) can be found here:  
http://ena-docs.readthedocs.io/en/latest/

## Step 1: Create an account on the EMBL-EBI ENA website
Go to the submission panel of ENA and create a login and password.    
https://www.ebi.ac.uk/ena/submit/sra/#home

## Step 2: Register your study/project to get an accession number e.g. PRJEB1234
This BioProject accession number will serve to record:
- The studies that you made under the same project (if you sequenced a genome and made different transcriptomic studies for instance under the same project)
- The samples that belong to the same study.

This project number will be asked by reviewers before any publication.  

Describe your study: "Transcriptomic of different whitefly organs"    
Provide an abstract.   
Provide a short title.  

Your study now gets an accession number. You can start to add samples. But before that, you need to upload the actual fastq files.

## Step 3: Upload samples to your private upload ENA area
First, the fastq files need to be in a [proper format](http://ena-docs.readthedocs.io/en/latest/format_01.html#standard-formats) and must be compressed using gzip or bzip2.
You can compress the original file using the Shell (these two options will also keep the original fastq file): 
- `gzip < file.fastq > file.fastq.gz` 
- `gzip -k file.fastq` 

There are a lot of possible options. I would recommend using the Webin file uploader system that runs Java on your computer.

http://ena-docs.readthedocs.io/en/latest/upload_01.html#using-webin-file-uploader
You first need to compress the fastq files so that they have a `.gz` extension for instance. Then select them and upload. They will be checksummed. 

## Step 4: add samples to your study.
Simply follow the guidelines on the website.
