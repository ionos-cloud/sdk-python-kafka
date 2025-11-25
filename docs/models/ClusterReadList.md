# ClusterReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID of the list of Cluster resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of Cluster resources. | 
**items** | [**list[ClusterRead]**](ClusterRead.md) | The list of Cluster resources. | [optional] 

## Example

```python
from ionoscloud_kafka.models.cluster_read_list import ClusterReadList

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterReadList from a JSON string
cluster_read_list_instance = ClusterReadList.from_json(json)
# print the JSON string representation of the object
print(ClusterReadList.to_json())

# convert the object into a dict
cluster_read_list_dict = cluster_read_list_instance.to_dict()
# create an instance of ClusterReadList from a dict
cluster_read_list_from_dict = ClusterReadList.from_dict(cluster_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


