# UserReadAccess


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the user. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the user. | 
**metadata** | [**UserAccessMetadata**](UserAccessMetadata.md) |  | 
**properties** | [**User**](User.md) |  | 

## Example

```python
from ionoscloud_kafka.models.user_read_access import UserReadAccess

# TODO update the JSON string below
json = "{}"
# create an instance of UserReadAccess from a JSON string
user_read_access_instance = UserReadAccess.from_json(json)
# print the JSON string representation of the object
print(UserReadAccess.to_json())

# convert the object into a dict
user_read_access_dict = user_read_access_instance.to_dict()
# create an instance of UserReadAccess from a dict
user_read_access_from_dict = UserReadAccess.from_dict(user_read_access_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


