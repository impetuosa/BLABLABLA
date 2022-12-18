# Modelling and understanding migrating applications: A dynamic model approach
In this folder, we find the elements required to reproduce the validating experiment in Mac/Intel installation. 
You can reproduce the experiment in Linux or windows, but for doing so it is required to adapt the **experiment.sh** to work on those technologies. 
If the paper is accepted we can do the extra effort of automatizing this process for windows and Linux and for publishing it in GitHub.

## The folder is organized as follows: 
* Fylgja10
	 - experiment.sh
     - Pharo.image    
	 - Pharo.changes
	 - Pharo10.0-64bit-570d7ba.sources
	 - pharo
	 - pharo-ui
	 - pharo-vm
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
In order to automatically reproduce the experiment you must open this folder in a terminal, step into the Fylgja10 folder, and execute the **experiment.sh** script.
The script is going to start the Pharo image with the Pharo virtual machine executing a Pharo program that instruments the experiment given a model path and an ontology path. 
This file is programmed to execute the Pharo image with all the combinations of the six models and the six previously extracted ontologies. 
For each experiment are going to export two files into the **logs** folder: one file with all the entities analysis and the other with all the relations.

The last step in the script analyses all the generated files and aggregates all the data into a table.csv file that can be further opened with any spreadsheet program.

## Paper experiment files 
In this folder, you are going to find the outcome of the experiment used for the paper.
The logs files (produced in each execution of the Pharo tool).
In the tabls.csv file, aggregation is calculated by analyzing the files. 
In the classToChange.csv file, we find the aggregation by type. 
The consolidation.xlsx, where we organize the data and graphics to show in the paper.
The transformations.xlsx, where we load the aggregation by type and organize it in tabs per project.


## Disclaimer
We want to insist on the fact that the EPaie project mode is not shipped, since it is a closed-source project. 
For what the experiment is not identical to the one exposed in the article.









