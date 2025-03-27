# data-analyst-saugat

Draw.io:

![Screenshot 2025-03-26 183315](https://github.com/user-attachments/assets/78541fb8-e686-4284-92e8-5fa35478c62c)


Descriptive Data Analysis of Community Food Markets and Farmers Markets. 

The research project conducts a descriptive analysis of both community food markets and farmers markets. 
Project Description: 
The research focuses on creating an understanding of community food market structures through descriptive analysis techniques applied to farmers markets. The research goal is to produce a condensed overview of operational information like market classifications and geographical locations together with operating hours and vendor participation and product listing. The data organization reveals patterns which demonstrate that markets operate most on specific days and operate continuously for certain months while particular goods tend to be the most popular vendor items. The analysis will create an organized overview which describes market functions for local communities and food accessibility support.

Project Title: 
Understanding Market Operations and Offerings in Local Community and Farmers Markets

Objective: 
The research conducts a data analysis of community food markets alongside farmers markets to establish market pattern connections between types, schedule times and vendor presence and product content. The obtained results enhance local food delivery services as well as outreach strategies. The findings aid governmental organizations and nonprofit institutions in making better choices which cultivate food stability alongside economic development. Future research about vendor diversity as well as market accessibility and coverage becomes possible because of the foundation this study provides. Through pattern analysis communities gain the ability to organize operations better and build better relationships with residents.
Dataset: 
This dataset contains information about various community food markets and farmers markets. The key features included are:
•	Year: The year the market was active
•	Market Type: Indicates whether it’s a community food market or a farmers market
•	Market Name / Location / Host: Name of the market, its location, and the hosting organization
•	Market Operator: The organization that operates the market
•	Street Number: The number part of the street address
•	Street Direction: The directional part of the street address (e.g., N, S, E, W)
•	Street Name: The name of the street
•	Street Type: Type of street (e.g., St, Ave)
•	Merged Address: Full street address
•	Market Direction: Additional location details or landmarks
•	Website: Web address for more information about the market
•	Day: The day(s) the market is held
•	Open: Market opening time
•	Close: Market closing time
•	Months: The months during which the market is in operation
•	Number of Vendors: Total number of vendors participating
•	Offerings: Types of goods sold (e.g., produce, meat, seafood, cheese, prepared foods)

Methodology: 
Data Collection: 
The project retrieved data from Amazon S3 through its CSV file named FoodMarket.csv which was structured within a directory path. Community food markets along with farmers markets formed the data points found in the dataset. The fm-ven-lst-cln-sau job in AWS Glue DataBrew performed cleaning operations on the data before analysis through standardization of columns and removal of null values and normalization of date-time fields with address consolidation. The cleaned dataset was saved to S3 after processing so it became ready for additional use and reporting.
Descriptive Analysis: 
The patterns in the community and farmers markets dataset were studied through descriptive statistical methods. The research analyzed market occurrence developments at annual, daily and monthly periods to uncover seasonal characteristics. Data was arranged according to market types and vendor count enabled the projection of market activity levels and size. Through these insights researchers gained fundamental knowledge about the long-term market operations. The research examined product category distribution through the "Offerings" field by studying regular items including produce, meat, seafood, prepared foods. Research on product patterns and combinations helped identify the most successful merchandise items. Without sales data the dataset still delivered knowledge regarding market structure and product availability and scheduling trends.

Data Visualization:
AWS Glue Studio enabled the creation of an ETL pipeline which transformed and filtered the cleaned data through updates to the schema and data aggregation techniques. Excel together with Amazon QuickSight and Python tools displayed the data results. The available dataset without time-of-day or sales data enabled the creation of visual representations which included bar charts for product categories alongside market types alongside day and month trend graphs. The visual representations made difficult information easier to understand while showing important data relationships.
Customer Segmentation: 
The research study grouped customers into segments through market types since it lacked access to personal customer information. A study conducted an operational comparison between Community Food Markets and Farmers Markets to evaluate their promotional characteristics and vendor support systems along with their offered products. Community Markets functioned during weekdays with few vendors present while Farmers Markets attracted customers through weekend operations with diverse products on sale. The market segmentation demonstrated that distinct market types satisfy unique customer requirements.
Insight Findings:
Most outlets including Farmers Markets functioned primarily during weekend days with Sunday being the most popular day while operating between May to October because of seasonal patterns and consumer preferences. Farmers Market customers could access more fresh local products but needed to use either cash or digital payment options. The different shopping needs of customers stemmed from the separate operational hours and goods available at Community Food Markets and Farmers Markets.
Recommendation:
The dataset confirms necessary conclusions for operational market enhancement and neighborhood involvement support. Organizers need to allocate additional vendors and inventory prior to weekends along with warmer months since markets show maximum activity at these times. Popular food items ranging from fresh produce to organics joined by prepared foods yield increased sales whereas special events and extended operating hours drive up customer attendance. The marketing approach of Community Food Markets includes support program partnerships whereas Farmers Markets target local seasonal products. Efficiency enhancement with better market reach will result from strategic digital payment expansion together with market type and customer preference alignment.

Tools and Technologies that I used in AWS:
1. Data Ingestion in S3 bucket:

![Community Farmers Market and Food Market Data Ingestion](https://github.com/user-attachments/assets/e6e6580d-f73a-4b06-ae75-d58e89bc97c9)

![S3 Buckets  Data Ingestion](https://github.com/user-attachments/assets/3c1acb73-2568-46cc-9037-98d48099ec13)


 
S3 folder structure showing fm-raw-sau path
A structured folder path allowed the transmission of FoodMarket.csv to Amazon S3 as part of the process. Storage organization alongside retrieval efficiency creates the data pipeline base during this step.

2. Data Profiling with AWS Glue DataBrew:

![Project  Data Profiling](https://github.com/user-attachments/assets/cfdf29ba-24dd-4c9c-ae30-ac65d0fd44ac)

 
The analysis and detection of data quality through outlier detection together with missing value identification and schema validation occurred using AWS Glue DataBrew. Data transformation occurs exclusively for records which meet the proper standards of formation.

3. Data Cleaning with AWS Glue DataBrew Job:
 
![Data Cleaning](https://github.com/user-attachments/assets/ecec2b66-3eb3-4504-9ab1-4825d4f685b3)


The process of data cleaning for removing duplicates and enforcing data types and handling null values was accomplished through jobs such as fm-ven-lst-cln-sau. After cleaning the data it was returned to S3 storage.

4. Data Summarization with AWS Glue:

![Data Summarization](https://github.com/user-attachments/assets/395aec4d-7516-48fb-808c-3502e8eb7378)

![ETL Pipeline design](https://github.com/user-attachments/assets/2ad841a2-97a9-4e1c-bdc9-0e3be85f77a1)


 
ETL pipelines performed summary operations on vendor data through filter-based aggregations. The structured datasets became ready for prediction applications through vendor behavior modeling thanks to these preparation steps.

5. Data Cataloging with AWS Glue Catalog: 
 
![Data Catalog](https://github.com/user-attachments/assets/53005e44-96ff-4acf-9154-d3225bf632c8)
![Data cataloging tables](https://github.com/user-attachments/assets/d2f1cad2-d5b4-4718-8ba1-8b6e1be050a5)


AWS Glue Crawlers both analyzed the data and created Glue Catalog metadata tables to enable users to search, access and analyze the dataset using Athena or Redshift.

6. Data Analysis in Amazon Athena:
 
![5](https://github.com/user-attachments/assets/2b454b5e-6d1f-4fe8-a122-250ba14195b8)
![4](https://github.com/user-attachments/assets/6a309a27-fddc-4316-817e-1ba8cbd481d3)


The stored processed data existed in CSV and Parquet formats for performance and operational flexibility. Amazon Athena provided users with a capability to run SQL queries on S3 data which generated insights related to market distribution and vendor trends and operations.

7. Data Security with S3, KMS and Replication:
 
![8](https://github.com/user-attachments/assets/804ea7c7-f20c-405b-8a28-53b7a1e58478)
![7](https://github.com/user-attachments/assets/c3e78e5e-8d44-420c-a3f3-dee0be621b4c)


SSE-KMS encryption combined with versioning and cross-bucket replication functions as the dataset security system. SSE-KMS encryption together with versioning and cross-bucket replication ensured dataset security and protected it from unauthorized modifications and unauthorized access.

8. Data Governance & Quality Check:
 
![10](https://github.com/user-attachments/assets/0a815947-323e-49e5-80db-0e42bcd5ae38)
![12](https://github.com/user-attachments/assets/26ffc8f4-0ed7-4247-9a6c-e97e149c94d2)
![11](https://github.com/user-attachments/assets/5aac7bb1-dcb5-44bb-93f8-c6c5eb422b91)



The validation process directed the data to either the “Passed” or “Failed” folders through application of quality standards. The platform's validation measure directed reliable data into specified folders which enhanced the quality of information for analyzes.

9. Monitoring with CloudWatch and CloudTrail:

 ![14](https://github.com/user-attachments/assets/59f2422d-50e2-47b8-992f-822fbf15ee97)
![13](https://github.com/user-attachments/assets/0503460e-a0c7-4bdb-b22c-3b558fc198d3)

 
The storage and usage metrics came under CloudWatch monitoring while CloudTrail tracked API activities for auditing purposes and compliance requirements. They gave real-time operational monitoring along with security oversight through their features.

10. Trend Visualization and Market Insight Over Time: 
 
![output (6)](https://github.com/user-attachments/assets/a37fb981-31bb-4995-a52a-43ba1206778b)


Visual analysis demonstrated changing market trends regarding growth and decline in various market types. The number of Farmers Markets stayed level but Community Food Markets expanded until policy changes led to their decrease.


Conclusion:
This project showcases the complete AWS-based data pipeline for Vancouver’s Community Food Market and Farmers Market datasets. The data entered Amazon S3 before being profiled and cleaned through AWS Glue DataBrew before Glue ETL summarized it for analysis. The AWS Glue Data Catalog served as the metadata management system so users could query their data through Amazon Athena. Security standards included S3 versioning in combination with KMS encryption and replication configuration. The data quality check process followed governance steps and CloudWatch alongside CloudTrail served as monitoring tools. Through this pipeline businesses obtain trustworthy secured operational findings about their local food markets that scale effectively.
