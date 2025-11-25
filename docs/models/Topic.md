# Topic

A topic is a category or feed name to which records are published. Topics are the way Kafka organizes messages. They act as logical channels for data streams. Topics are split into partitions, making them scalable and allowing parallelism. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of the Kafka cluster topic. Must be 63 characters or less and must begin and end with an alphanumeric character (&#x60;[a-z0-9A-Z]&#x60;) with dashes (&#x60;-&#x60;), underscores (&#x60;_&#x60;), dots (&#x60;.&#x60;), and alphanumerics between.  | 
**replication_factor** | **int** | The number of replicas of the topic. The replication factor determines how many copies of the topic are stored on different brokers. The replication factor must be less than or equal to the number of brokers in the Kafka cluster.  | [optional] [default to 3]
**number_of_partitions** | **int** | The number of partitions of the topic. Partitions allow for parallel processing of messages.  | [optional] [default to 3]
**log_retention** | [**TopicLogRetention**](TopicLogRetention.md) |  | [optional] 

## Example

```python
from ionoscloud_kafka.models.topic import Topic

# TODO update the JSON string below
json = "{}"
# create an instance of Topic from a JSON string
topic_instance = Topic.from_json(json)
# print the JSON string representation of the object
print(Topic.to_json())

# convert the object into a dict
topic_dict = topic_instance.to_dict()
# create an instance of Topic from a dict
topic_from_dict = Topic.from_dict(topic_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


