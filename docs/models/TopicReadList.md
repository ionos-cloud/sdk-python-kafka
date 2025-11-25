# TopicReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID of the list of Topic resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of Topic resources. | 
**items** | [**list[TopicRead]**](TopicRead.md) | The list of Topic resources. | [optional] 

## Example

```python
from ionoscloud_kafka.models.topic_read_list import TopicReadList

# TODO update the JSON string below
json = "{}"
# create an instance of TopicReadList from a JSON string
topic_read_list_instance = TopicReadList.from_json(json)
# print the JSON string representation of the object
print(TopicReadList.to_json())

# convert the object into a dict
topic_read_list_dict = topic_read_list_instance.to_dict()
# create an instance of TopicReadList from a dict
topic_read_list_from_dict = TopicReadList.from_dict(topic_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


