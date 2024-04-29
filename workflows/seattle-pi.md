---
layout: default
title: Seattle Post-Intelligencer Collection
parent: Workflows
nav_order: 1
---
# Seattle Post-Intelligencer Collection
This page documents the steps for MOHAI's current digital preservation project with the Seattle Post-Intelligencer Collection. 

The basic structure of this workflow is to transfer content from obsolete physical storage media to server-based storage, understand and ingest the transferred content, generate integrity information for all relevant content, package content with relevant metadata and other relevant file information, store content in a secured environment with clear parameters about who can read, write, and access the content, and perform regular fixity checks of the content.

## Transfer Content off of Optical Media
* Required: [Nimbie Autoloader](https://sophiebassfryelibrary.github.io/digarch/tools/equipment-nimbie.html) + [IROMLAB](https://sophiebassfryelibrary.github.io/digarch/tools/software-programs.html#fixity-pro)
  
## File Format Identification
* **Required**: [DROID](https://sophiebassfryelibrary.github.io/digarch/tools/software-programs.html#droid)

### Opening and preparing DROID
* Open DROID by clicking DROID.bat using the digital preservation workstation.
* Install any updates that may pop up on the opening screen to ensure you are working with the newest information.
* Go to Tools > Preferences.
* Under Profile Defaults, check Select Generate Hash for Each File using MD5.
* Under Signature Updates > Update Settings, select "Every time DROID starts up."
* Click OK to save these settings.

### Creating a profile
* Click New
* Click File > Save As
* Select a Location and name your profile using the DROID profile naming convention (2007_107_Box Number)
* Click Save
* Click Add
* Select Folder (All subfolders are included)
* Click OK
* Click Save to save the profile with the folder(s) included

### Running DROID and exporting data
* To start your file analysis, click Start
* Click the plus sign next to the folder to see the analysis results
* Click the Export button
* Select the DROID profile you wish to export, and click Export Profiles
* Select a save location and select CSV as the filetype
* Name the file using the DROID profile naming convention (2007_107_Box Number) and click Save
* Click OK
* Exported data will be included in the batch bag.

### Creating DROID reports
* Click on the Report tab
* Select Generate Report
* Select the profile(s) you’d like to report on
* Select a report type using the Select Report menu
* Report types include Comprehensive Breakdown, File count and sizes, File count and sizes by file format PUID, File count and sizes by mime type, File count and sizes by month last modified, File count and sizes by year and month modified, File count and sizes by year last modified, Total count of files and folders, Total unreadable files, and Total readable files
* Select Report on profiles
* The report should now be displayed; click Export to save the report.
* Select a save location and give the report a name
* Select PDF and click Save
* Click Close to exit
* Include relevant reports in batch bag


## Bag Content
* **Required**: [Bagger](https://sophiebassfryelibrary.github.io/digarch/tools/software-programs.html#bagger)

  
## Perform Automated Fixity Checks
* **Required**: [Fixity Pro](https://sophiebassfryelibrary.github.io/digarch/tools/software-programs.html#fixity-pro)

### Start and name a new project
* Click New Project
* Assign the Project a name using the naming convention
* Select MD5 checksum application
* Click Create

### Add the folders to be checked
* Click Add Directory
* Select the type of storage to be checked: Internal, External, or Network
* Navigate to the desired folder and click Open to add it to the project
* Click Add Filter to exclude a file type from the integrity check
* Type the extension of the filetype you wish to exclude from the integrity check; click OK to add to a project.

### Input the email addresses for emailing reports
* Click Add Report Recipient Email to add relevant email(s) to add the email address(es) that should receive reports on the integrity checks.
* Type the recipient's email address and click Add.

### Schedule the integrity checks
* Under Schedule the Scan, select the frequency at which checks will be carried out (Monthly, Weekly, Daily, or Manual)
* Select the day of the week you would like to schedule the scan
* Select a time for the scan to run
* Click Save Project and OK
* To run a scan manually, click Manual Scan.
* Each check runs its comparison against the previous check
* If errors are discovered and fixed, run a new manual check to reestablish the correct checksums.
