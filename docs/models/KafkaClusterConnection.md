# KafkaClusterConnection

Connection information of the Kafka cluster. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**datacenter_id** | **str** | The datacenter to connect your instance to. | 
**lan_id** | **str** | The numeric LAN ID to connect your instance to. | 
**broker_addresses** | **list[str]** | IP addresses and subnet of cluster brokers. Note the following unavailable IP range: 10.224.0.0/11  | 

## Example

```python
from ionoscloud_kafka.models.kafka_cluster_connection import KafkaClusterConnection

# TODO update the JSON string below
json = "{}"
# create an instance of KafkaClusterConnection from a JSON string
kafka_cluster_connection_instance = KafkaClusterConnection.from_json(json)
# print the JSON string representation of the object
print(KafkaClusterConnection.to_json())

# convert the object into a dict
kafka_cluster_connection_dict = kafka_cluster_connection_instance.to_dict()
# create an instance of KafkaClusterConnection from a dict
kafka_cluster_connection_from_dict = KafkaClusterConnection.from_dict(kafka_cluster_connection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


