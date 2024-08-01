About Dataset

Details
This dataset contains the details of over 11,000 athletes, with 47 disciples, along with 743 teams that were taking part in Tokyo Olympics 2020- 2021.

It contains data set of athletes, coaches, and teams participating as well as entries by gender. It contains names, countries, disciplines, gender and names of the coaches as well.

Credits
Source : Tokyo Olympics 2020 Website



The following peroject we are working on is to ingest the data from on prem SQL database ( i.e. our dataset), use Azure Data Factory (ADF) for data ingestion, then push it into Azure Data 
Lake, transform the data using Databricks and then use Azure synapses for data analysitcs and also use visualization tools such as power Bi for visualiation and dashboarding.


1. Created a resource on azure portal with name : tokyo-olympic-data. Added 2 folders : namely raw-data and transformed-data.
2. Created a ADF with name : tokyo-olympic-df-####2511.
3. Created a copy data (with name data-ingestion) for ingesting data.
4. Taking data from git hub (we can use kaggle too, but requires more work than git, hence taking git)
5. Take the URL of each file from the git hub ( 5 files ) and we need to select that as a source for the data-ingestion process so we can extraxt data from here.
6. IMP : Since raw format is only being downloaded and not giving raw url, convert it into raw url for the files to be attached
7. Next, we require a ADLS ( Azure Data Lake Storage ) , to store the data and create it fro all 5 csv files
8. Validate to check for no errors and same use the button debug.
9. Next , create a databricks workspace with name : tokyo-olympic-db
10. We need to register an app to create the connection between the "raw-data" we have already pushed into azure, and databricks
11. We need to create secret client and key ( also copy paste the client ID and Tenant ID on a notepad for future reference)
12. We need these values for the connection from adure data factory to databricks
13. Passing the value as it is, is a bad practice, for this we can use the 'key vault' feature of azure to keep it hidden
14. To create the connection , we need to pass client id, secretkey, tenant id, and then also provide mount id ( here using syntax of container_name@storage_account and for mount 
    name use any name and then try to establish the connection on databricks console.
15. We also need to provide role access for the app, using stroage and IAM.

