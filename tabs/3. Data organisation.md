---
layout: default
title: 3. Data Organisation
nav_order: 4
---


# Chapter 3: Open Data in Neuroscience
**Authors: Mar Barrantes-Cepas, Eva van Heese;**
**Reviewers: Janneke Lemmerzaal**
## DATA DEFINITION
## Data Definition 

First, what is data? Neuroscience data encompasses everything you use or produce during your research life, from datasets, software, code, workflow, models, figures, tables, articles, etc. Everything contains a piece of information, such as brain imaging techniques (for instance, MRI, PET, EEG, MEG), cognitive and behavioural data, and cellular, histological, and molecular evaluations of brain samples from humans or animals. All this research and clinical data follows a lifecycle (https://the-turing-way.netlify.app/reproducible-research/rdm/rdm-data) that involves data creation, use, publication and sharing, archiving, and re-use or destruction. 
ADD FIGURE FORM TURING WAY!!!! 
The scope of the present chapter includes data organisation and sharing, all information related to software, code, and workflows is explained in Chapter 4.  
Personal data
Personal data in neuroscience refers to an individual's personal information that can identify the person, i.e. birth date, raw MRI scan, security number, etc. The use of personal data has significant implications for privacy and ethical considerations. Personal data are not always as evident or accessible as we think. For example, DICOM headers might contain the person’s name or date of birth, or from structural MRI scans, we can easily identify the person’s face if it’s not defaced (see software and tools in Chapter 4). As researchers, we must ensure responsible handling of personal data, by anonymizing our data properly in case of storing and sharing it, following the ethical protocols. If you're allowed to share data, you may also consider sharing metadata or documentation as part of your transparency efforts. We advise you to consult with the legal department of your institution before sharing anything. 
Documentation and Metadata
	For datasets
Data available with no context that cannot be understood is of no use. However, metadata and documentation can provide provenance and context to datasets. Therefore, you should ensure that any dataset, but especially open datasets, includes consistent metadata and documentation that provides insightful information about how the data was collected. Metadata is often intended for machine reading, but some forms are human-readable. Basic metadata can be described on the level of the dataset (title, study summary, keywords, contact information, licence) and data elements (variable name, description, unit, modification date). Advanced metadata may describe the frequency of updates, temporal coverage (cross-sectional, longitudinal, follow-up duration), and spatial coverage (i.e. geographic area). 
	For data processing and analysis
For data processing and analysis, keeping organised and descriptive documentation about the step-by-step process is key. Whereas everyone generally does this in their own manner, the movement of open data and open scripting has set some standards on how to improve documentation for yourself and others. A couple of essential elements to include in your documentation are:
a summary of the general steps (i.e from raw data to outcome)
for example in a flowchart
the software, automated pipelines, scripts or other tools applied
specify version, platform, and other environmental details
specify decisions made (manual settings)
for code: provide examples from your actual code
correctly cite these tools and their documentation
troubleshooting: issues you encountered and their solutions
describe common mistakes
describe steps that require a cautious approach
cite solutions or workarounds provided online
quality assessment
which checks should and could be performed?
how does good/bad data look? provide examples (images!)

Documentation will look different for each analysis and can be described in many formats: a (shared) document, spreadsheet, or environment that allows for files and code to be incorporated (for example Github). Important is that the documentation can be understood by anyone (with the expected background knowledge) and used as a guide to perform the analysis described. 

Creative Commons and data licensing
Licenses provide a standardized way for others to use your creative work under copyright legislation. The different Creative Commons (CC) licenses describe what permissions the public has to do with your work. The license types are formed by combinations of sharing principles:
BY: credit must be given to the creator
NC: only non-commercial uses of the work are permitted
SA: Adaptations must be shared under the same terms
ND: No derivatives or adaptations of the work are permitted
Together, they result in six license types (CC BY-SA, CC BY-NC, CC BY-NC-SA, CC BY-ND, CC BY-NC-ND). A seventh license type (CC Zero or CC0) allows the creator to give up their copyright and all public users to adapt, build upon, and distribute the original work without any conditions. You can consult the online tool Licence Chooser from CC if you struggle to choose a license for your work. Interested to read more about CC licenses? Check out this page. 
DATA MANAGEMENT PLAN
How to manage your data is usually described in a Data Management Plan (DMP). It provides information on six main topics: (i) roles and responsibilities, (ii) type and size of the data collected and documentation or metadata generated, (iii) type of data stored used and backup procedures that are in place, (iv) preservation of the research outputs after the project, (v) re-use of your research outputs by others and (vi) costs (see more details at https://the-turing-way.netlify.app/reproducible-research/rdm/rdm-dmp#rr-rdm-dmp). 
Before creating your own DMP, we recommend consulting with your institution to see if they have a specific template for the DMP. If you are from the Amsterdam UMC, please check https://www.amsterdamumc.org/en/research/support/services-facilities/data-management/data-management-plan-dmp.htm Moreover, we recommend creating a checklist/roadmap before starting your research with the steps that need to be performed in order to make your project as according to open science principles, and the requirement or things you need to check for each step. For example, can everyone from your team understand how the data is organised or where to find it with the minimum knowledge? More information can be found at: https://the-turing-way.netlify.app/reproducible-research/rdm/rdm-checklist or in the case of Amsterdam UMC  https://www.amsterdamumc.org/en/research/research-roadmap.htm  
FAIR PRINCIPLES 
It's recommended to follow the FAIR principles in data for improving Findability, Accessibility, Interoperability, and Reusability. If you plan it from the beginning, it is easier to make data FAIR (https://the-turing-way.netlify.app/reproducible-research/rdm/rdm-fair). Making data FAIR is not the same as making it open. Keep in mind that data should be as open as possible and as closed as necessary. Accessible means that there is a procedure in place to access the data that could benefit sharing data or methods within your own group or department and re-use existing pipelines without having to put much effort into finding data. 
DATA STORAGE AND ORGANISATION
Storing your data correctly is important to prevent data loss, which happens more often than we would like. To avoid data loss, it’s recommended to pick a suitable storage system and back up your data frequently. Your institution will usually provide information on how to store your data. Consult which are the different storage systems your institution is using and how you can back up data correctly. You can either consider using cloud storage if your data protection allows it or you can consider encrypting your data before storage.  
At the same time, organising data in a meaningful and FAIR way may be challenging, especially at the beginning of new projects where we are not fully sure of all the intermediate files. You should use a clear folder structure to ensure you can find your files. 
In the following paragraphs, we divided our recommendations depending on which kind of neuroscience data you are mainly working with brain imaging (MRI, PET, EEG, MEG), cognitive, behavioural, cellular, histological, or molecular data. 
Brain Imaging Data Standards
Brain Imaging Data Standards (BIDS) is a community-driven consensus on how to organise and share data obtained in neuroimaging experiments (everybody can become part of the community). Lack of consensus led to time wasted on rearranging data or rewriting scripts in a certain way. More information about the guidelines and specifications can be found at https://bids.neuroimaging.io/ or https://bids-specification.readthedocs.io/en/stable/index.html
	BIDS project folder structure
Briefly, each project has a main folder containing a sourcedata, rawdata and derivatives folder, where different types of data will be stored. Sourcedata is meant to be for data before any kind of conversion, reconstruction and/or harmonisation, rawdata is expected to contain the data converted to NIFTI and JSON format, and finally, derivatives should contain all the files derived from your analysis. 
