# Protocols related to the Sequence Server

This small protocol describes how to access the Sequence Server BLAST server gathering wild tomato sequence information.

Link to the sequence server --> to be added.

## How to add a nucleotide database 
1. Log in to the head node `h0` of the genseq compute system: `ssh genseq-h0.science.uva.nl`  
2. Go to the folder containing the Sequence Server databases: `cd /zfs/datastore0/system/databases/blastserver`
3. Add your fasta file there: `mv myfastafile.fasta ./` 
4. Format your fasta file into an NCBI blast database: `makeblastdb -dbtype nucl -in LA4024.fasta  -title Solanum_lycopersicum_LA4024_denovo -parse_seqids`. 
Make sure you give it a human-readable title and to parse the sequence identifiers.
5. Restart the sequence server:
  - first stop it: `kilall sequenceserver`
  - restart the server: `scl enable rh-ruby23 sequenceserver &`

# Sequence Server references
* http://sequenceserver.com/  
* https://www.biorxiv.org/content/10.1101/033142v1
