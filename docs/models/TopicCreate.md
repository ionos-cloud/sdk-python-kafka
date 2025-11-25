# TopicCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Topic**](Topic.md) |  | 

## Example

```python
from ionoscloud_kafka.models.topic_create import TopicCreate

# TODO update the JSON string below
json = "{}"
# create an instance of TopicCreate from a JSON string
topic_create_instance = TopicCreate.from_json(json)
# print the JSON string representation of the object
print(TopicCreate.to_json())

# convert the object into a dict
topic_create_dict = topic_create_instance.to_dict()
# create an instance of TopicCreate from a dict
topic_create_from_dict = TopicCreate.from_dict(topic_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


