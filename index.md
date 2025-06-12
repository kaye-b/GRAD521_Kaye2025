# Data description
In 2023, the University of Washington and the King County Regional Housing Authority (KCRHA) implemented a network-based survey method for estimating the number of people experiencing homelessness, which includes those experiencing doubled-up homelessness. This survey resulted in a dataset containing network, demographic, health and needs assessment data from 1,100+ people experiencing homelessness in the Seattle area in 2023. 

Survey data was collected by volunteer at community resource hubs, like libraries and daytime shelters. Volunteers used tablets to help participants fill out a UW Qualtrics survey form. All volunteers went through sensitivity and harm reduction training so they knew how to have respectful and empathetic interactions with survey respondents. Volunteers were also trained on software tools and survey methods to ensure accurate data collection.

The two types of data for this project consist of 1) the raw survey data, and 2) R scripts used to work with the data.

The raw survey data consists of approximately 1,100 rows and 90 columns, some of which are derived. R scripts will be created to clean, transform and analyze the survey data. The size of the raw survey data and R scripts combined is <1 GB.

# Roles and responsibilities
2 PIs at the University of Washington (UW) are responsible for implementing the DMP for the project. PIs are part of the University of Washington Homelessness Count Project (UWHCP) team and roles and responsiblities are assigned from within the UWHCP team.
* Data manager, DMP implementation and quality control – PIs, with some quality control assigned to other UWHCP project leads
* Protection of sensitive and protected data, access control –  PIs control access to data–see below for trainings required for data access.
* Data collection/data generation – PIs led data collection efforts, with other UWHCP members, including research scientists, graduate students, agency partners and volunteers, participating in the effort to collect data. The Data Science for Social Good (DSSG) team, along with graduate students and post-docs, will be primarily responsible for generating scripts to clean, process and analyze data.
* Data organization, metadata generation, data analysis, software creation and maintenance – PI leads with graduate students and other researchers responsible for this work as it relates to individual projects using the data. 
* Archiving and preservation – PIs, with option to assign to research assistants and graduate students.

If either of PIs for this project leaves UW, the responsibility for the data will remain with the other PI and with the Center for Studies in Demography and Ecology (CSDE) at UW. Any of the above roles assigned to a PI or other person leaving the project will be reassigned from within the CSDE.

# Data standards and metadata
## Metadata
Metadata will be created to document (1) dataset variables and (2) all data processing and analysis scripts.

Variables will be documented using a codebook, modeled on Data Documentation Initiative (DDI) metadata standards, with information on each variable, including the full range of values or categories, data type, description, details on missing data and source. The codebook will also record how variables were cleaned or transformed, and note any derived variables. Initial codebook will be created after data cleaning, using the R package dataMaid, with additionaly notes about data cleaning added manually. Codebook will be updated with any derived variables created as a part of analyses.

Documentation of functions and analyses will be through a README.md file in the repository that shows file structure, describes the purpose of each script, and explains how scripts and functions interact to produce derived datasets and final outputs. This document will be drafted and updated as scripts and analyses are added to the main repository.

After functions and analysis are complete, the R package roxygen2 will be used to provide more formal documentation that clarifies inputs, outputs, and dependencies for each function.

# Storage and security
Survey data and R scripts will be stored on secure servers managed by the (CSDE) at UW. Data stored on the servers is in CSV and R files. No copies of raw data are allowed and data can only be accessed via the CSDE servers, with access restricted via dual-authentication password protection. Access to the CSDE servers when not connected to the UW network requires the use of Husky OnNet -- an individual VPN service that provides a secure connection to the UW network from remote locations.

Raw survey data will be protected from loss by backup copies maintained on separate servers. R scripts will be protected from loss by version control software (Git) and remote storage via GitHub. These softwares protect against accidental data loss by preserving a full history of changes and ensuring cloud backup of all scripts. Researchers using the data will make it a practice to commit changes often to avoid accidental data loss.

## Data organization
Data organization will primarily consist of labeling and organizing scripts (functions and analyses). File structure will consist of a project folder with the following subfolders and files:

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

# Access and data sharing
Data access will be managed by the University of Washington Homelessness Count Project (UWHCP) team.
Data access is restricted for the confidentiality of research participants and because of funder requirements. These protections restrict the ability to share raw data, however data can be shared in the aggregate (averages, totals, etc.). 

Because of restrictions to protect the confidentiality of research participants, data will not be made publicly available. Access to the raw data is granted through a data use agreement, managed by the University of Washington Homelessness Count Project (UWHCP) team (Project leads: Zach Almquist and Nathalie Williams). All researchers wanting access to the data must 1) participate in the interviewer training at UW and 2) complete basic training in human subject protection. 

Aggregated data has been made publicly available in summary tables and charts on GitHub (<a href="https://uwescience.github.io/DSSG2024_understanding_homelessness/" target="_blank"> 2024 Data Science for Social Good “Understanding Homelessness” project </a>).

R Code for analyses and metadata (which will make use of a subset of the data) will be shared with the research group via a GitHub repository. Access to GitHub repository and code will be managed by the UWHCP team under the same data use agreement as the raw data.
Any publication that uses the data must cite the UWHCP team using the following format:

Zack Almquist, Amy Hagopian, Paul Hebert, Nathalie Williams and UWHC Project Team (2023). UW Seattle area homelessness count Project, Center for Studies in Demography and Social Ecology, University of Washington.

# Archiving and preservation
Data will be archived indefinitely on secure servers managed by The Center for Studies in Demography and Ecology (CSDE) at the University of Washington. (Find out more...)
