# Submission metabolic datasets to the EMBL-EBI Metabolights repository
[MetaboLights](https://www.ebi.ac.uk/metabolights/index) is a database for Metabolomics experiments and derived information.   
The database is cross-species, cross-technique and covers metabolite structures and their reference spectra as well as their biological roles, locations and concentrations, and experimental data from metabolic experiments. MetaboLights is the recommended Metabolomics repository for a number of leading journals.

## Create an environment to run Java versions
To run the ISA creator tool that runs in Java, you need to install up to date java versions.  

I personnally use [Conda](https://conda.io/docs/), a software and package manager. 
You can install it by downloading and installing [Anaconda](https://conda.io/docs/) on your machine.

To run Conda and install java versions into a dedicated environment:         
`conda install -c anaconda java-1.7.0-openjdk-cos6-x86_64`  
`conda install -c cyclus java-jre `  

## Run the ISA creator software
### Download the ISA creator suite
Please download the complete zip file at "ftp://ftp.ebi.ac.uk/pub/databases/metabolights/submissionTool/ISAcreatorMetaboLights.zip" (copy paste the link into your favorite web browser).

### Launch the executable  
Navigate to the downloaded folder ("ISAcreatorMetaboLights.zip").  
Launch the executable: 
- Windows ( with Java installed) `run_WIN.cmd`
- Windows( without Java installed) `run_WIN_WITH_JAVA.cmd`
- Linux `run_LINUX.sh`
- Mac OS: `run_MAC.command`

