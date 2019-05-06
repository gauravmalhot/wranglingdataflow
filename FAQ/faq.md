FAQs
===============================

1. What are the supported regions for Wrangling data flow?

   Wrangling data flow is currently supported in data factories created in following regions:
   1. East US.
   2. Southeast Asia
   
   ** Other regions are coming in shortly.
   
2. What are the limitations and contraints with Wrangling data flow?

   1. Only Azure Data Lake Storage Gen2 (with only CSV and JSON format) is supported as source dataset.
   2. Source dataset linked service should only have MSI/Service principal based auth (Key auth based linked service support is coming shortly).
   3. Sink dataset should only refer to key auth based linked service.
   4. Staging linked service should only be key auth based.
   5. Wrangling dataflow activity must have a staging linked service referenced.
