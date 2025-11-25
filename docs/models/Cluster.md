# Cluster

A Kafka cluster that stores data and serve client requests. Kafka clusters typically have multiple brokers to handle more data and provide high availability. Each broker is identified by a unique ID and manages partitions of different topics. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of your Kafka cluster. Must be 63 characters or less and must begin and end with an alphanumeric character (&#x60;[a-z0-9A-Z]&#x60;) with dashes (&#x60;-&#x60;), underscores (&#x60;_&#x60;), dots (&#x60;.&#x60;), and alphanumerics between.  | 
**version** | **str** | The version of Kafka. Allowed values are &#x60;3.7.0&#x60; and &#x60;3.8.0&#x60;. Deprecation Warning: &#x60;3.7.0&#x60; will be removed end of May 2025.  | 
**size** | **str** | The size of your Kafka cluster. The size of the Kafka cluster is given in T-shirt sizes. Valid values are: &#x60;XS&#x60;, &#x60;S&#x60;, &#x60;M&#x60;, &#x60;L&#x60;, and &#x60;XL&#x60;.  | 
**connections** | [**list[KafkaClusterConnection]**](KafkaClusterConnection.md) |  | 

## Example

```python
from ionoscloud_kafka.models.cluster import Cluster

# TODO update the JSON string below
json = "{}"
# create an instance of Cluster from a JSON string
cluster_instance = Cluster.from_json(json)
# print the JSON string representation of the object
print(Cluster.to_json())

# convert the object into a dict
cluster_dict = cluster_instance.to_dict()
# create an instance of Cluster from a dict
cluster_from_dict = Cluster.from_dict(cluster_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


