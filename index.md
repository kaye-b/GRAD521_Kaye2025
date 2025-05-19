# Data description
In 2022, the University of Washington and the King County Regional Housing Authority (KCRHA) implemented a network-based method for estimating the number of people experiencing homelessness, which includes those experiencing doubled-up homelessness. The initial pilot project was followed by a larger pilot study conducted in 2023, resulting in two datasets containing network, demographic and needs assessment data from 1,100+ people experiencing homelessness in the Seattle area in 2023. 

* Dataset #1 - Survey and network data from ~850 individuals experiencing homelessness in Seattle. Variables collected include basic demographics, location of previous night’s sleep (shelter, tent, car, with a friend, in a park, etc.), veteran status, substance use and mental health, and support services needed.

* Dataset #2 - Survey and network data from ~250 individuals experiencing homelessness in the great Puget Sound area. This dataset was collected by a different researcher using similar methodology with a more extensive set of survey questions.

I will primarily be working with a merged dataset, that pulls from both datasets, keeps common variables, and accounts for individuals that appear in both surveys. 

# Roles and responsibilities
2 PIs at the University of Washington (UW) are responsible for implementing the DMP for the project. Below are some of the DMP roles and the primary person or people responsible: 
* Data manager, DMP implementation and quality control – primarily PIs though some quality control may be assigned to other project leads, such as researcher assistants and graduate students. 
* Protection of sensitive and protected data, access control –  PIs control access to data–see below for training required before researchers can access data through secure servers.
* Data collection/data generation – PIs led data collection efforts, with other research scientists and graduate students leading the effort to organize data collection and train volunteers and students for survey data collection.
* Data organization, metadata generation, data analysis, software creation and maintenance – PI leads with graduate students and other researchers responsible for much of this work as it relates to individual projects using the data. 
* Archiving and preservation – primarily the PIs, but also may be assigned to a research assistants and graduate students

# Data standards and metadata
## Data organization
Data organization for my project will primarily consist of labeling and organizing scripts (functions and analyses). File structure will consist of a project folder with the following subfolders and files:

<ul>
  <li>main_project_folder/
    <ul>
      <li>import_clean_folder/
        <ul>
          <li>Scripts to merge RDS and PSD data sets</li>
          <li>Scripts to clean data, transform variables, and derive columns</li>
          <li>Scripts for creating Respondent Driven Sampling data frame</li>
        </ul>
      </li>
      <li>exploration_folder/
        <ul>
          <li>Scripts with basic summaries, plots, distributions</li>
        </ul>
      </li>
      <li>analysis_folder/
        <ul>
          <li>Scripts for analysis (may be subdivided by analysis focus)</li>
        </ul>
      </li>
      <li>visualizations_folder/
        <ul>
          <li>Scripts with publication-quality visualizations</li>
        </ul>
      </li>
      <li>products_folder/
        <ul>
          <li>Reports, markdown files, and other products</li>
        </ul>
      </li>
    </ul>
  </li>
</ul>


## Tracking versions
I will use Git for version control to track changes in my scripts, with GitHub as the remote repository where updates will be pushed to the main branch for other researchers to access.

## Metadata
Metadata will primarily be to document 1) variables and 2) functions and analysis. 

For documenting variables, I will create a detailed codebook, modeled on Data Documentation Initiative (DDI) metadata standards, with information on each variable, including the full range of values or categories, data type, description, details on missing data and source. The codebook will also record how variables were cleaned or transformed, and note any derived variables. Initial codebook will be created after data cleaning and before analyses and will be updated with any derived variables created as a part of analyses.

Documentation of functions and analyses will be through a README.md file in the repository that shows file structure, describes the purpose of each script, and explains how scripts and functions interact to produce derived datasets and final outputs. This document will be drafted and updated as scripts and analyses are added to the main repository.

Functions and analysis will also be documented with in-line comments as they are created. Potentially I will include structured documentation after functions and analysis are complete, such as with the roxygen2 package in R, to clarify inputs, outputs, and dependencies for each function.


# Storage and security

# Access and data sharing
Data used in this project needs to be protected for the confidentiality of research participants and because of funder requirements. The project is funded in part by the National Institute of Health (NIH), which requires that researchers working with data on human subjects must comply with the NIH’s Human Subjects Education Policy and undergo education in the protection of human subjects in research. 

These protections restrict the ability to share raw data, however data can be shared in the aggregate (averages, totals, etc.).

Because of restrictions to protect the confidentiality of research participants, data will not be made publicly available. Access to the raw data is granted through a data use agreement, managed by the University of Washington Homelessness Count Project (UWHCP) team (Project leads: Zach Almquist and Nathalie Williams). All researchers wanting access to the data must 1) participate in the interviewer training at UW and 2) complete basic training in human subject protection. 

Aggregated data has been made publicly available in summary tables and charts on GitHub (<a href="https://uwescience.github.io/DSSG2024_understanding_homelessness/" target="_blank"> 2024 Data Science for Social Good “Understanding Homelessness” project </a>).

R Code for analyses and metadata for my capstone project (which will make use of a subset of the data) will be shared with the research group via a GitHub repository. Access to GitHub repository and code will be managed by the UWHCP team under the same data use agreement as the raw data.
Any publication that uses the data must cite the UWHCP team using the following format:
Zack Almquist, Amy Hagopian, Paul Hebert, Nathalie Williams and UWHC Project Team (2023). UW Seattle area homelessness count Project, Center for Studies in Demography and Social Ecology, University of Washington.

# Archiving and preservation
Data will be archived indefinitely on secure servers managed by The Center for Studies in Demography and Ecology (CSDE) at the University of Washington. Access will be managed by the UWHCP team. Data stored on the servers is in CSV and R files. No copies of raw data are allowed – data can only be accessed on the CSDE servers.
