FAQs
================================

1. What are the supported regions for Wrangling data flow?

   Wrangling data flow is currently supported in data factories created in following regions:
   1. Australia East
   2. Canada Central
   3. Central India
   4. East US
   5. East US 2
   6. Japan East
   7. North Europe
   8. Southeast Asia
   9. South Central US
   10. UK South
   11. West Central US
   12. West Europe
   13. West US
   14. West US 2

2. What are the limitations and constraints with Wrangling data flow?
   1. Following type of V2 datasets are supported:
      1. Azure BLOBs (CSV format only) -> Account key based auth.
      2. Azure Data Lake Storage Gen2 (CSV format only) -> Account key and Service Principal based auth.
      3. Azure SQL DB/DW -> UserName/Password auth. Refer https://github.com/gauravmalhot/wranglingdataflow/blob/master/FAQ/Supported%20SQL%20Types for supported SQL data types.
      4. Azure Data Lake Storage Gen1 (CSV format only) -> Service Principal based auth
   2. Sink dataset should only be v2 dataset types.
   3. No polybase/staging support for SQL DW.
   4. Key Vault support for linked services in not supported
   5. Source dataset names can only be alpha-numeric

3. What is the difference between Mapping and Wrangling Data Flow?

   Mapping Data Flows in ADF provide a way to transform data at scale without any coding required. You can design a data transformation job in the data flow designer by constructing a series of transformations. Start with any number of source transformations followed by data transformation steps. Then, complete your data flow with sink to land your results in a destination. Mapping Data Flow is great at mapping via column map and transform from a known-unknown left side set of data sets to a known-unknown right side (e.g. pull a bunch of data and blend them to populate a dimensional model).

   Wrangling Data Flow in ADF allows you to do agile data preparation/exploration. It enables the familiar Power Query Online mashup editor to do data preparation but now at scale via spark execution. With the rise of data lakes sometimes you just need to explore a data set or you are just asked to create a dataset in the lake that has all customer demographic info for new customers since 2017. In this case you are not mapping to a known target , you are just exploring data sets to meet the requirement and then you will publish it in the lake.  These are often used for less formal/modelling analytics scenarios (i.e. data engineer built a data set for ad hoc analysis, data engineer is operationalizing a self-service project built by an information worker, etc.).

4. What is the difference between Power Platform Dataflows and Wrangling Data Flow?
   
   Power Platform Dataflows allow business users (citizen data analysts and app developers) to seamlessly import and transform data from a wide range of data sources into the Common Data Service and Azure Data Lake, in order to build PowerApps applications, Power BI reports or Flow automations. Power Platform Dataflows leverage the familiar Power Query data preparation experiences, which these users already know and feel comfortable with, from Power BI and Excel. Power Platform Dataflows also enable ease reuse within an organization and automatically handle orchestration (e.g. automatically refreshing dataflows that depend on another dataflow when the former one is refreshed).

   Azure Data Factory (ADF) is a managed data integration service that allows Data Engineers/Citizen Data Integrator to create complex hybrid extract-transform-load (ETL), extract-load-transform (ELT), workflows. Wrangling Data Flow (WDF) in ADF empowers users with a code-free, serverless environment that simplifies data preparation in the cloud and scales to any data size, no infrastructure management required. It uses the industry leading Power Query data preparation technology (also used in Power Platform dataflows, Excel, Power BI) to seamlessly prepare/shape the data. Built to handle all the complexities and scale challenges of big data integration, Wrangling Data Flows allow users to quickly prepare data at scale via spark execution. Users can build resilient data pipelines in an accessible visual environment with our browser-based designer and let ADF handle the complexities of Spark execution. Build schedules for your pipelines and monitor your data flow executions from the ADF monitoring portal. Easily manage data availability SLAs with ADF’s rich availability monitoring and alerts and leverage built-in CI/CD capabilities to save and manage your flows in a managed DataOps environment. And establish alerts and view execution plans to validate that your logic is performing as planned as you tune your data flows.
