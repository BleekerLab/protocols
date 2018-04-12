# Protocol to archive datasets (part of Research Data Management)
If you wonder how to archive sequencing or other datasets, here's a couple of way to do it.

# At SURF Archive
You should dispose of a user name and a password granted by SURFsara for their [Data Archive](https://www.surf.nl/en/services-and-products/data-archive/index.html) service.   
The datasets will be archived on a Tape Archive. 

Note1: this protocol can also be used to save other valuable datasets. 
Note2: files should be zipped in one single archive (``files.gzip`` or ``files.tar.gz``) before being sent to Data Archive.

## Option 1: using the ``scp`` protocol
1. On the command-line, open a new window
2. Compress the files that you want to send. If your sequencing files are in a folder named ``fastq_files_20180120/`` then archive this folder into ``fastq_files_20180120.tar.gz``  
3. Type ``scp fastq_files_20180120.tar.gz [yourusernamename]@archive.surfsara.nl:~/project1/data/`` 
4. Type your password
4. The transfer should start straight away. Your archived file will be in ``~/project1/data/`` on your account at SURFsara Data Archive.

For instance, for me, a typical command would be ``scp myfastqfiles.tar.gz mgalland@archive.surfsara.nl:~/project1/data/``. Your password would be requested after pressing enter. 

## Option 2: using a FTP client such as FileZilla
If you don"t like the command line, you can use a client for that. 

# Using the SILS Tape Archiver
A tape (DELL Ultrium6) costs 30€ and can store 2.5TB (uncompressed native files) or up to 6.25TB (compressed files) per tape.  

The SILS Tape Archiver is meant to save datasets that are either: 
- the whole workspace from a PhD student, a postdoc or a student.
- big datasets where no common standard repository is available. For instance, a series of images that are too big for FigShare or Zenodo and that cannot be stored in a standard repository such as the EBI-ENA. 

Thanks to the SILS Tape Archive, a whole workspace can be saved and your are able to go back to original datasets

It is meant to be used at the end of the project. 

You will have a primary (one copy of the archive) and one copy belongs to the group that generated it. 

1. Submit a request for an identifier at http://sils-tape.science.uva.nl/requestform.php
2. If your request is accepted, you will get an identifier and a location where to save your dataset. You can now upload datasets (compressed or not).
3. If below 6.25TB, then it fits on one tape. Otherwise, divide the dataset into several files, each < 6.25TB.   
4. Upload it using via ``ssh`` protocol or through a ftp client such as CyberDuck.
5. An archive copy is made. Then the group copy is also created that can be stored by the Principal Investigator. 

The complete RDM data protocol can be found [here](https://github.com/BleekerLab/protocols/blob/master/bioinformatics/UvA-FNWI-SILS-dataprotocol.v5.pdf).

# At Zenodo 
Multiple datasets can be uploaded to [Zenodo](https://zenodo.org/).Each dataset must be <50Gb but more can be requested.  
Zip your file one by one and upload them. You will have to describe the experiment info: collectively these are called __metadata__ or "data about the data" which help to make sense of your experiment afterwards.  
More info [here](http://help.zenodo.org/)

# EBI European Nucleotide Archive (ENA)
The standard for genomic datasets.
