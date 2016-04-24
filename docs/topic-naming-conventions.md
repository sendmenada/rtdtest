##Topic Naming Conventions
###Draft

Guidelines for defining topic names in Kafka:

**[_root namespace_].[_product_].[_type_].[_stage_]** 
where: 
**.** or period is the separator 

**[_root namespace_]** is a 3 letter representation of a business unit such: 

* **cor** for core or infrastructure topic that is shared across units

* **rad** for Research And Development (TPS)

* **veg** for Vegetable

* **bio** for BioTech 

* **com** for Commercial

* **usr** for user or developer testing topic 

**[_product_]** is the application/product producing the topic

**[_type_]** is the product type or data set name 

**[_stage_]** is the processing stage or statistic, such as _validated_ | _testingX_ | _incoming_ | _filtered_ | _duplicate_ | _clean_ | _clickrate_ | _bot_ | _error_
 
For example, **_cor.remedy.ticket-log.incoming_** would represent an _infrastructure/core topic_ for _Remedy data_ on the _Ticket Logging data set_ and an _incoming data stream_. If there is further downstream processing, then the next step might be validating the data in which case that topic would be named **_cor.remedy.ticket-log.validated_**.