# TopicRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Topic. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Topic. | 
**metadata** | [**ResourceMetadata**](ResourceMetadata.md) |  | 
**properties** | [**Topic**](Topic.md) |  | 

## Example

```python
from ionoscloud_kafka.models.topic_read import TopicRead

# TODO update the JSON string below
json = "{}"
# create an instance of TopicRead from a JSON string
topic_read_instance = TopicRead.from_json(json)
# print the JSON string representation of the object
print(TopicRead.to_json())

# convert the object into a dict
topic_read_dict = topic_read_instance.to_dict()
# create an instance of TopicRead from a dict
topic_read_from_dict = TopicRead.from_dict(topic_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


