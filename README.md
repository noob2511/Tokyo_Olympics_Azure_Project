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
5. 
