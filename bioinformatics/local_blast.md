# How to perform a blast locally on your own computer.
From NCBI Blast:

> BLAST (Basic Local Alignment Search Tool) is a set of similarity search programs designed to explore all of the available sequence databases regardless of whether the query is protein or DNA. The BLAST programs have been designed for speed, with a minimal sacrifice of sensitivity to distant sequence relationships. The scores assigned in a BLAST search have a well-defined statistical interpretation, making real matches easier to distinguish from random background hits. BLAST uses a heuristic algorithm which seeks local as opposed to global alignments and is therefore able to detect relationships among sequences which share only isolated regions of similarity (Altschul et al., 1990). 

Most things come NCBI directly: [find it here](https://www.ncbi.nlm.nih.gov/books/NBK52640/)

# Installation and setup of the blast program

## Install Miniconda3 

1. Navigate to the [Miniconda installer webpage](https://docs.conda.io/en/latest/miniconda.html)
2. Download and install the one for your operating system (e.g. Windows).
3. Start a Shell and run `bash Miniconda3-latest-MacOSX-x86_64.sh` (example given for Mac OS X).
4. Follow the installation procedure and answer the questions asked.

## Install NCBI Blast using conda

In your Shell:
1. If conda is properly installed, then you can type: `conda --version` and you should get a number speciyfing the version number of conda.
2. It's a good practice to create a dedicated environment separated from your base environment. Do this: `conda env create --name blast -c bioconda blast`. This will install the latest version of ncbi blast. 
3. Activate this enviromnent: `conda activate blast`

# Format the blast database
You know need to create a blast database. It converts a FASTA file into a custom blast database format.

1. Do you have a FASTA file? Check that it is a correctly formatted FASTA file.
2. Run this in bash: 

`makeblastdb -in [path/to/your/fastafile] -dbtype [nucl for nucleotides / prot for proteins] -parse_seqids`

3. You can check your blast database with the `blastdbcheck` command.

For a nucleotide database, you should have 
Remark: do not try to make a blast db from the NCBI non-redundant nucleotide or protein databases. They are too big. You have to download the pre-formatted databases.
NCBI blast databases can be found at ftp://ftp.ncbi.nlm.nih.gov/blast/db/

# Run the blast
## For a nucleotide blast
To check which version of the blastn program that you have, type: `blastn -version`

To get a complete list of all options, type `blastn -h`

### (very) basic usage of blastn.`
This will send all results to the standard output (your screen) without any formatting
`blastn -db path/to/your/blastdb -query path/to/your/query/fasta/file`

### More advanced usage of blastn
What you can do is set up some optional values to get a more precise view.
*  `-db` the path to your database (path to your blast formatted database). Example: ~/myblastdb/test.fasta (the blast database will be composed of `<test.fasta.nhr test.fasta.nin test.fasta.nsq>`) 
*  `-query` the path to your fasta file query
*  `-out` a path to a file that will contain all blast results. This file will be created.
*  `-evalue` the expect value (E) is a parameter that describes the number of hits one can "expect" to see by chance when searching a database of a particular size.  
*  `-word_size` the BLAST algorithm uses "words" to nucleate regions of similarity. The default Word size for a protein sequence is 3 residues and for nucleotide sequences it is 11 bp. A blastn search will not work with a word size of less than 7. Set it to 7 for short sequences like PCR primers.
*  `-max_hsps` A High-scoring Segment Pair (HSP) is a local alignment with no gaps that achieves one of the highest alignment scores in a given search. Set this number to 1 to get only one HSP per subject
*  `-outfmt` a number (0 to 11) that corresponds to an output format option. Please see below for a complete description.
*  `-max_target_seqs`  this option doesn't specify the maximum number of hits per query, but the maximum number of target sequences for hits per query.
*  `-num_threads` number of computer cores (CPU) to be used. Check first how many you have on your local machine (e.g. usually four on a Mac)

### Outformat types (`-outfmt`)
alignment view options:
*  0 = pairwise,
*  1 = query-anchored showing identities,
*  2 = query-anchored no identities,
*  3 = flat query-anchored, show identities,
*  4 = flat query-anchored, no identities,
*  5 = XML Blast output,
*  6 = tabular,
*  7 = tabular with comment lines,
*  8 = Text ASN.1,
*  9 = Binary ASN.1,
*  10 = Comma-separated values,
*  11 = BLAST archive format (ASN.1) 

Options 6, 7, and 10 can be additionally configured to produce a custom format specified by space delimited format specifiers.
The supported format specifiers are:
*  qseqid means Query Seq-id
*  qgi means Query GI
*  qacc means Query accesion
*  qaccver means Query accesion.version
*  qlen means Query sequence length
*  sseqid means Subject Seq-id
*  sallseqid means All subject Seq-id(s), separated by a ';'
*  sgi means Subject GI
*  sallgi means All subject GIs
*  sacc means Subject accession
*  saccver means Subject accession.version
*  sallacc means All subject accessions
*  slen means Subject sequence length
*  qstart means Start of alignment in query
*  qend means End of alignment in query
*  sstart means Start of alignment in subject
*  send means End of alignment in subject
*  qseq means Aligned part of query sequence
*  sseq means Aligned part of subject sequence
*  evalue means Expect value
*  bitscore means Bit score
*  score means Raw score
*  length means Alignment length
*  pident means Percentage of identical matches
*  nident means Number of identical matches
*  mismatch means Number of mismatches
*  positive means Number of positive-scoring matches
*  gapopen means Number of gap openings
*  gaps means Total number of gaps
*  ppos means Percentage of positive-scoring matches
*  frames means Query and subject frames separated by a '/'
*  qframe means Query frame
*  sframe means Subject frame
*  btop means Blast traceback operations (BTOP)

When not provided, the default value is:

'qseqid sseqid pident length mismatch gapopen qstart qend sstart send evalue bitscore', which is equivalent to the keyword 'std'
 
 Default outformat option is __'0'__

## For a protein blast
Type `blastp -h`
