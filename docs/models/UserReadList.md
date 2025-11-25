# UserReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID of the list of User resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of User resources. | 
**items** | [**list[UserRead]**](UserRead.md) | The list of User resources. | [optional] 

## Example

```python
from ionoscloud_kafka.models.user_read_list import UserReadList

# TODO update the JSON string below
json = "{}"
# create an instance of UserReadList from a JSON string
user_read_list_instance = UserReadList.from_json(json)
# print the JSON string representation of the object
print(UserReadList.to_json())

# convert the object into a dict
user_read_list_dict = user_read_list_instance.to_dict()
# create an instance of UserReadList from a dict
user_read_list_from_dict = UserReadList.from_dict(user_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


