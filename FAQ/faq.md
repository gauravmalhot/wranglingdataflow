FAQs
================================

1. What are the supported regions for Wrangling data flow?

   Wrangling data flow is currently supported in data factories created in following regions:
   1. East US.
   2. Southeast Asia

   ** Other regions are coming in shortly.

2. What are the limitations and constraints with Wrangling data flow?

   1. Only Azure Data Lake Storage Gen2 (with only CSV and JSON format) is supported as source dataset.
   2. Sink dataset should only be v2 dataset types (of CSV and JSON format).
   2. Sink dataset should only refer to key auth based linked service.
   3. Staging linked service should only be key auth based.
   4. Wrangling dataflow activity must have a staging linked service referenced.
   5. Wrangling data flow is currently not supported in GIT mode.

3. What is the difference between Mapping and Wrangling Data Flow?

   Mapping Data Flows in ADF provide a way to transform data at scale without any coding required. You can design a data transformation job in the data flow designer by constructing a series of transformations. Start with any number of source transformations followed by data transformation steps. Then, complete your data flow with sink to land your results in a destination. Mapping Data Flow is great at mapping via column map and transform from a known left side set of data sets to a know right side (e.g. pull a bunch of data and blend them to populate a dimensional model).

   Wrangling Data Flow in ADF allows you to do agile data preparation/exploration. It enables the familiar Power Query Online mashup editor to do data preparation but now at scale via spark execution. With the rise of data lakes sometimes you just need to explore a data set or you are just asked to create a dataset in the lake that has all customer demographic info for new customers since 2017. In this case you are not mapping to a known target , you are just exploring data sets to meet the requirement and then you will publish it in the lake.  These are often used for less formal/modelling analytics scenarios (i.e. data engineer built a data set for ad hoc analysis, data engineer is operationalizing a self-service project built by an information worker, etc.).
