# Protocol to archive sequencing datasets to SURF Archive
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

## Option 2: using a FTP client 
