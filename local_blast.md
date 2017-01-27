# How to perform a blast locally on your own computer.

# Installation and setup of the blast program
## get the latest NCBI blast program.

[Latest blast program for Mac Os X](ftp://ftp.ncbi.nlm.nih.gov/blast/executables/LATEST/ncbi-blast-2.6.0+.dmg) (for Mac Os X)

## Install it on your computer. 

Start a bash session [more help here](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
The computer has to know where to find the blast program. What you need to do is to edit your "PATH" variable.When running a bash session:

1.  Type in `nano ~/.bash_profile
2.  Add this line: `<export PATH=$PATH:$HOME/ncbi-blast-2.2.29+/bin>`__Important_: here the path points to your home directory.
You can put the program anywhere on your computer as long as you know where to put it.
3. check that it worked: `<echo $PATH>`

# Format the blast database
You know need to create a blast database. It converts a FASTA file into a custom blast database format.

1. Do you have a FASTA file? Check that it is a correctly formatted FASTA file.
2. Run this in bash: `<makeblastdb -in [path/to/your/fastafile] -dbtype [nucl for nucleotides / prot for proteins] parse_seqids>`
3. You can check your blast database with the `<blastdbcheck>`command.

Remark: do not try to make a blast db from the NCBI non-redundant nucleotide or protein databases. They are too big. You have to download the pre-formatted databases.
NCBI blast databases can be found [here](ftp://ftp.ncbi.nlm.nih.gov/blast/db/)

# Run the blast
## For a nucleotide blast
Type `<blastn -h>`

## For a protein blast
Type `<blastp -h>`
