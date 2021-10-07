covidPhenotype
==============================

<img src="https://img.shields.io/badge/Study%20Status-Repo%20Created-lightgray.svg" alt="Study Status: Repo Created">

- Analytics use case(s): **Phenotyping Covid**
- Study type: **Descriptive**
- Tags: **Phenotype**
- Study lead: **Gowtham Rao**
- Study lead forums tag: **Gowtham_Rao(https://forums.ohdsi.org/u/Gowtham_Rao)**
- Study start date: **10/07/2021**
- Study end date: **10/21/2021**
- Protocol: **-**
- Publications: **-**
- Results explorer: **-**

Description
==============================
This is a Cohort Diagnostics study that aims to evaluate cohort definitions for covid over a network of data sources.

Requirements
============

- A database in [Common Data Model version 5](https://github.com/OHDSI/CommonDataModel) in one of these platforms: SQL Server, Oracle, PostgreSQL, IBM Netezza, Apache Impala, Amazon RedShift, Google BigQuery, or Microsoft APS.
- R version 4.0.0 or newer
- On Windows: [RTools](http://cran.r-project.org/bin/windows/Rtools/)
- [Java](http://java.com)
- 25 GB of free disk space

How to run
==========
1. Follow [these instructions](https://ohdsi.github.io/Hades/rSetup.html) for setting up your R environment, including RTools and Java. 

2. Open your study package in RStudio. Use the following code to install all the dependencies:

	```r
	renv::restore()
	```

3. In RStudio, select 'Build' then 'Install and Restart' to build the package.

3. Once installed, you can execute the study by modifying and using the code provided under `extras/CodeToRun.R`

4. Upload the file ```export/Results_<DatabaseId>.zip``` in the output folder to the study coordinator:

	```r
	uploadResults(outputFolder, privateKeyFileName = "<file>", userName = "<name>")
	```
	
	Where ```<file>``` and ```<name<``` are the credentials provided to you personally by the study coordinator.
		
5. To view the results, use the Shiny app:

	```r
	launchDiagnosticsExplorer()
	```
  
  Note that you can save plots from within the Shiny app. 

License
=======
The covidPhenotype package is licensed under Apache License 2.0

Development
===========
covidPhenotype was developed in ATLAS and R Studio.

### Development status

Unknown
