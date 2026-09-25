# Sierra ILS Collection Development - Billed Items Automated Report
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/python-%233670A0.svg?style=for-the-badge&logo=python&logoColor=ffdd54)

## Summary
**What it does:** This automated report identifies items billed between 30 and 60 days ago.

**Impact:** Empowers collection development librarians by automatically delivering a scheduled report, every 30 days, that includes actionable insights on items to consider for repurchase.

## Features and Deliverables

**Automated Email:**

<img width="952" height="631" alt="Monthly Billed Items Email" src="https://github.com/user-attachments/assets/e3efae5c-4ceb-4576-ba64-b6fff5be795d" />

**Attached Excel Report:**

<img width="1380" height="964" alt="Billed-Items" src="https://github.com/user-attachments/assets/609e2500-d7f2-4879-bb42-47d34f5d8f89" />

<img width="1377" height="985" alt="Billed-Items" src="https://github.com/user-attachments/assets/79162cc8-2e57-4c82-b1ac-0070100ca72d" />


## Data Pipeline Architecture
This repository features an automated data pipeline that generates, formats, and distributes Excel reports via email. The system integrates Windows Task Scheduler, a Batch script, SQL, and Python to handle the end-to-end workflow without manual intervention. The automated process is fully productionized within a Windows environment.

**Workflow Overview:**

[Windows Task Scheduler] ──> [orchestrator.bat] ──> [main.py] ──> [Sub-modules & SQL] ──> [Report delivered to Email Inbox]

**Repository Contents & Security Note:**

To comply with data security policies, the core Python automation scripts have been omitted from this public repository. Instead, this repository provides:
- The SQL Data-Extraction Script: The exact logic used to pull and aggregate Sierra ILS production data.
- Manual Alternative: If you do not have an automated environment, you can run the provided SQL script manually in pgAdmin and export the results directly to a spreadsheet.

## Acknowledgments
The automated pipeline is built off the brilliant work of Gem Stone-Logan. For more information on implementing the automated system, please see her IUG presentations, [Automating Reports with Python.](https://www.gemstonelogan.com/presentations.html)
