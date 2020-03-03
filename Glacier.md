# Glacier

Expedited retrievals allow you to quickly access your data when occassional urgent requests for a subet of archives are required. For all but the largest archives (250MB+), data access using Expedited retrievals are typcically made available within 1-5 mintues. Provisioned Capacity ensures that retrieval capacity for Expedited retrievals is available when you need it.

to make an Expedited, Standard, or Bulk retrieval, set the Tier parameter in the Initiate Job (POST jobs) REST API request to the option you want, or the equivalent in the AWS CLI or AWS SDKs. If you have purchased provisioned capacity, then all expedited retrivals are automatcially served through your provisioned capacity

Provisioned Capacity ensures that your retrieval capacity for expedited retrivals is available when you need it. EAch unit of capacity provides that at least three expedited retrivals can be performed every five minutes and provides up to 150MB/s of retrival throughput. You should purchase provisioned retrieval capacity if your workload requires highly reliable and predictable access to a subset of your data in minutes. Without provisioned capacity Expedited retrievals are accepted, except for rarae situations of unusually high demand. However, if you require access to Expedited retrievals under all circumstances, you must purchase provisioned retrieval capacity.
