SQL Scripts
This folder contains 2 sub folders. 
Multisite Tables.txt: This will have tables needed for aggregating the data in the multisite database along with a control table 
Load_Control : This table acts as a driver table for the Master workflow and holds the source container and destination database information.

Tables And Views for Tenant Database.txt: This file contains all the tables and views needed for Tenant database which can be deployed to any number of Tenant databases like Site1, Site2....Siten

Steps:

1. Connect to your Azure SQL server with Tenant Databases and Multisite database 
2. Run the 2 Scripts in their respective databases and update the load_control table with your naming conventions
3. Grant permissions to data factory managed identity
4. Upload sample data files into your data lake containers
5. Login to Azure Datafactory and kick off Master Workflow and make sure the pipeline executes all the steps with a success status
6. Debug at each individual pipeline level if something fails for easy maintainance
