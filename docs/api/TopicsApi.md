# ionoscloud_kafka.TopicsApi

All URIs are relative to *https://kafka.de-fra.ionos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clusters_topics_delete**](TopicsApi.md#clusters_topics_delete) | **DELETE** /clusters/{clusterId}/topics/{topicId} | Delete Topic
[**clusters_topics_find_by_id**](TopicsApi.md#clusters_topics_find_by_id) | **GET** /clusters/{clusterId}/topics/{topicId} | Retrieve Topic
[**clusters_topics_get**](TopicsApi.md#clusters_topics_get) | **GET** /clusters/{clusterId}/topics | Retrieve all Topics
[**clusters_topics_post**](TopicsApi.md#clusters_topics_post) | **POST** /clusters/{clusterId}/topics | Create Topic


# **clusters_topics_delete**
> clusters_topics_delete(cluster_id, topic_id)

Delete Topic

Deletes the specified topic.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://kafka.de-fra.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_kafka.Configuration(
    host = "https://kafka.de-fra.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_kafka.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_kafka.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_kafka.TopicsApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the cluster.
    topic_id = 'ae085c4c-3626-5f1d-b4bc-cc53ae8267ce' # str | The ID (UUID) of the topic.

    try:
        # Delete Topic
        api_instance.clusters_topics_delete(cluster_id, topic_id)
    except Exception as e:
        print("Exception when calling TopicsApi->clusters_topics_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the cluster. | 
 **topic_id** | **str**| The ID (UUID) of the topic. | 

### Return type

void (empty response body)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Deleting topic was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**409** | ### Conflict The request could not be completed due to a conflict with the current state of the resource.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_topics_find_by_id**
> TopicRead clusters_topics_find_by_id(cluster_id, topic_id)

Retrieve Topic

Returns the topic by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.topic_read import TopicRead
from ionoscloud_kafka.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://kafka.de-fra.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_kafka.Configuration(
    host = "https://kafka.de-fra.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_kafka.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_kafka.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_kafka.TopicsApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the cluster.
    topic_id = 'ae085c4c-3626-5f1d-b4bc-cc53ae8267ce' # str | The ID (UUID) of the topic.

    try:
        # Retrieve Topic
        api_response = api_instance.clusters_topics_find_by_id(cluster_id, topic_id)
        print("The response of TopicsApi->clusters_topics_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TopicsApi->clusters_topics_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the cluster. | 
 **topic_id** | **str**| The ID (UUID) of the topic. | 

### Return type

[**TopicRead**](TopicRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting topic was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**409** | ### Conflict The request could not be completed due to a conflict with the current state of the resource.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_topics_get**
> TopicReadList clusters_topics_get(cluster_id)

Retrieve all Topics

This endpoint enables retrieving all topics using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.topic_read_list import TopicReadList
from ionoscloud_kafka.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://kafka.de-fra.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_kafka.Configuration(
    host = "https://kafka.de-fra.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_kafka.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_kafka.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_kafka.TopicsApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the cluster.

    try:
        # Retrieve all Topics
        api_response = api_instance.clusters_topics_get(cluster_id)
        print("The response of TopicsApi->clusters_topics_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TopicsApi->clusters_topics_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the cluster. | 

### Return type

[**TopicReadList**](TopicReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested topics successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**409** | ### Conflict The request could not be completed due to a conflict with the current state of the resource.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_topics_post**
> TopicRead clusters_topics_post(cluster_id, topic_create)

Create Topic

Creates a new topic.
The full topic needs to be provided to create the object.
Optional data will be filled with defaults or left empty.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.topic_create import TopicCreate
from ionoscloud_kafka.models.topic_read import TopicRead
from ionoscloud_kafka.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://kafka.de-fra.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_kafka.Configuration(
    host = "https://kafka.de-fra.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_kafka.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_kafka.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_kafka.TopicsApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the cluster.
    topic_create = ionoscloud_kafka.TopicCreate() # TopicCreate | Topic to create.

    try:
        # Create Topic
        api_response = api_instance.clusters_topics_post(cluster_id, topic_create)
        print("The response of TopicsApi->clusters_topics_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TopicsApi->clusters_topics_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the cluster. | 
 **topic_create** | [**TopicCreate**](TopicCreate.md)| Topic to create. | 

### Return type

[**TopicRead**](TopicRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Topic successfully created. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**409** | ### Conflict The request could not be completed due to a conflict with the current state of the resource.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

