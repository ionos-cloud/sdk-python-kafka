# TopicLogRetention


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**retention_time** | **int** | This configuration controls the maximum time we will retain a log before we will discard old log  segments to free up space.  This represents an SLA on how soon consumers must read their data. If set to -1,  no time limit is applied.  | [optional] [default to 604800000]
**segment_bytes** | **int** | This configuration controls the segment file size for the log. Retention and cleaning is always done a file at a time so a larger segment size means fewer files but less granular control over retention.  | [optional] [default to 1073741824]

## Example

```python
from ionoscloud_kafka.models.topic_log_retention import TopicLogRetention

# TODO update the JSON string below
json = "{}"
# create an instance of TopicLogRetention from a JSON string
topic_log_retention_instance = TopicLogRetention.from_json(json)
# print the JSON string representation of the object
print(TopicLogRetention.to_json())

# convert the object into a dict
topic_log_retention_dict = topic_log_retention_instance.to_dict()
# create an instance of TopicLogRetention from a dict
topic_log_retention_from_dict = TopicLogRetention.from_dict(topic_log_retention_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


