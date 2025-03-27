# incrementaloadbootcamp5
Incremental Data Loading and Notifications
Bootcamp Project - 5

Overview
This project involves working with Azure Data Factory (ADF) to implement data ingestion and notification pipelines. The project will cover the following scenarios:
Incremental Data Load and Process Tracking: Load data incrementally into Azure SQL Database and update a tracking table.
Time-Based Notification: Send a notification if the pipeline succeeds or fails during a specific time window.
Data Ingestion and Team Notification: Ingest data from an SQL database into Azure Data Lake Storage and notify the data engineering team via Slack/Teams.

![Architecture Diagram](https://github.com/parthshah0311/incrementaloadbootcamp5/raw/main/images/Incremental%20Data%20Loading%20and%20Notifications.jpg)

Role Description:

As a Data Engineer, I was responsible for designing, implementing, and maintaining data pipelines and workflows using Azure Data Factory (ADF). My role focuses on automating data ingestion, transformation, and processing from various data sources to Azure SQL Database and Azure Data Lake Storage. Additionally, I am responsible for managing and optimizing workflows for incremental data loading and real-time notifications.

Key Responsibilities:

Incremental Data Loading: I design and implement pipelines that incrementally load data from external systems into Azure SQL Database while tracking the processing status in control tables.

Time-Based Notifications: I configure and automate notifications using Slack or Microsoft Teams to alert stakeholders about pipeline success or failure within a specific time window.

Data Transformation: I use Azure Data Factory Data Flow to perform data cleansing and transformations, ensuring data is optimized for downstream processing and analytics.

Monitoring and Optimization: I monitor the performance of data pipelines, resolve failures, and ensure efficient execution by leveraging ADF monitoring tools and logs.

Version Control & Collaboration: I manage and version my ADF pipeline code through integration with GitHub for version control, collaborating with the team to ensure best practices.

Documentation & Deployment: I write clear documentation for pipeline configurations, create ARM templates for deployment, and ensure pipelines are tested and successfully merged into the main branch.

![MyResource](https://github.com/parthshah0311/incrementaloadbootcamp5/raw/main/images/Resourcegroup.png)

Scenario 1: Incrementally Load Data and Mark as Processed
Objective:
Incrementally load data from an external system into Azure SQL Database. After each load, a stored procedure will execute to mark the records as processed or update the status in a tracking table.
Pipeline Setup:
Lookup Activity:
Retrieve the last processed timestamp from a control table to identify where to start the incremental load.
Copy Data Activity:
Ingest new records from the external system based on the timestamp.
Stored Procedure Activity:
Execute a stored procedure to update the control table and mark records as processed in the destination database.

![IncrementalPipeline](https://github.com/parthshah0311/incrementaloadbootcamp5/raw/main/images/incrementalpipeline.png)

Phase 1 - Changes for Scenario 1
Connect to GitHub Repo:


Configure Azure Data Factory to connect with your GitHub repository for version control and collaboration.
Switch to feature/jira-122 Development Workspace:


Switch to or create the feature/jira-122 branch within ADF for development purposes.
Peer Validation:
![PeerValidation](https://github.com/parthshah0311/incrementaloadbootcamp5/blob/raw/images/peerview.png)

Conduct a peer review of the work in the development workspace (feature/jira-122). Ensure that a new workspace is created for feature development, or use the existing QA workspace for testing.
Merge into Main Branch:


After successful testing, merge changes from feature/jira-122 into the main branch.
Publish ARM Templates in ADF Publish Branch:


Publish the ARM templates to the publish branch of your GitHub repository for deployment.
![PeerValidation](https://github.com/parthshah0311/incrementaloadbootcamp5/raw/main/images/pullandmergeintomain.png)

