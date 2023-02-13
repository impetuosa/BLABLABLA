# Understanding the Migration of Applications with Typing Ontologies
In this folder, we find the elements required to reproduce the validating experiment.
The experiment is designed to work on MacOS, Linux and Windows. However, to make it work in Windows you will need Cygwin or MinGW, as the launching scripts are written in bash. 

## Extracting zip files 

All the folders are zipped, as GitHub has restrictions for file sizes. 
Please unzip the three zip files: Binaries.zip, moxingmodels.zip and ontologies.zip

The experiment expects the existence of the folders moxingmodels and ontologies and should be accessible from the Binaries folder using the relative path ../moxingmodels and ../ontologies. Have this into account if you are willing to move the folders around. 



## The folder is organised as follows: 
* Binaries
	 - experiment.sh
	 - get-pharo.sh
     - Pharo.image    
	 - Pharo.changes
	 - Pharo10.0-64bit-570d7ba.sources
	 - logs 
* moxingmodels
	- access.moxing.northwind.ston
	- java.moxing.argouml.ston
	- java.moxing.petstore.ston
	- pharo.moxing.calypso.ston
	- pharo.moxing.moose.ston
* ontologies
	- access.ontology.epaie.ston
	- access.ontology.northwind.ston
	- java.ontology.argouml.ston
	- java.ontology.petstore.ston
	- pharo.ontology.calypso.ston
	- pharo.ontology.moose.ston
* paper-experiment-files 

## Running the experiment
To reproduce the experiment, you must open this folder in a terminal and step into the Binaries folder. 
### The Binaries folder
Our experiment is developed in Pharo 10. 
We find a Pharo 10 image in this folder with its changes and source file.
In this folder, we also have the experiment.sh file, the script which launches multiple experiments. 

### Getting Pharo virtual machine

You will need first to obtain a Pharo 10 virtual machine. To do so, execute the script get-pharo.sh. 
This script depends on wget and bash commands. 

This will download and extract the Pharo 10 virtual machine with its launching scripts. 

### Launching the experiment 

Within the folder Binaries, execute the experiment script **./experiment.sh**.
The script will start the Pharo image with the Pharo virtual machine executing a Pharo program that instruments the experiment given a model path and an ontology path. 
This file is programmed to execute the Pharo image with all the combinations of the six models and the six previously extracted ontologies. 
For each experiment are going to export two files into the **logs** folder: one file with all the entities analysis and the other with all the relations.

The last step in the script analyses all the generated files and aggregates all the data into a table.csv file that can be further opened with any spreadsheet program.

### Browsing the source code
Within the folder, Binaries execute **./pharo-ui Pharo.image**. This will open a Pharo image from the command line. 
Once the image pops up, use the system browser to find the packages **Moxing**, the ASG project, and **Spinoza**, the Typing Ontology project. 


## Paper experiment files 
In this folder, you will find the experiment's outcome used for the paper.
The logs files (produced in each execution of the Pharo tool).
In the tabls.csv file, aggregation is calculated by analysing the files. 
In the classToChange.csv file, we find the aggregation by type. 
The consolidation.xlsx, where we organise the data and graphics to show in the paper.
The transformations.xlsx, where we load the aggregation by type and organise it in tabs per project.


## Disclaimer
We want to insist that the EPaie project mode is not shipped since it is a closed-source project. 
The experiment is not identical to the one exposed in the article.









