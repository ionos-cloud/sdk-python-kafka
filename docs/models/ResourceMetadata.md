# ResourceMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_date** | **datetime** | The ISO 8601 creation timestamp. | [optional] [readonly] 
**created_by** | **str** | Unique name of the identity that created the resource. | [optional] [readonly] 
**created_by_user_id** | **str** | Unique id of the identity that created the resource. | [optional] [readonly] 
**last_modified_date** | **datetime** | The ISO 8601 modified timestamp. | [optional] [readonly] 
**last_modified_by** | **str** | Unique name of the identity that last modified the resource. | [optional] [readonly] 
**last_modified_by_user_id** | **str** | Unique id of the identity that last modified the resource. | [optional] [readonly] 
**resource_urn** | **str** | Unique name of the resource. | [optional] [readonly] 
**state** | **str** | State of the resource. Resource states: &#x60;AVAILABLE&#x60;: There are no pending modification requests for this item. &#x60;BUSY&#x60;: There is at least one modification request pending and all following requests will be queued. &#x60;DEPLOYING&#x60;: The resource is being created. &#x60;FAILED&#x60;: The creation of the resource failed. &#x60;UPDATING&#x60;: The resource is being updated. &#x60;FAILED_UPDATING&#x60;: An update to the resource was not successful. &#x60;DESTROYING&#x60;: A delete command was issued, and the resource is being deleted.  | 
**message** | **str** | A human readable message describing the current state. In case of an error, the message will contain a detailed error message.  | [optional] 

## Example

```python
from ionoscloud_kafka.models.resource_metadata import ResourceMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceMetadata from a JSON string
resource_metadata_instance = ResourceMetadata.from_json(json)
# print the JSON string representation of the object
print(ResourceMetadata.to_json())

# convert the object into a dict
resource_metadata_dict = resource_metadata_instance.to_dict()
# create an instance of ResourceMetadata from a dict
resource_metadata_from_dict = ResourceMetadata.from_dict(resource_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


