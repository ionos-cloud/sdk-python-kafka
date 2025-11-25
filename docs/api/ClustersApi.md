# ionoscloud_kafka.ClustersApi

All URIs are relative to *https://kafka.de-fra.ionos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clusters_delete**](ClustersApi.md#clusters_delete) | **DELETE** /clusters/{clusterId} | Delete Cluster
[**clusters_find_by_id**](ClustersApi.md#clusters_find_by_id) | **GET** /clusters/{clusterId} | Retrieve Cluster
[**clusters_get**](ClustersApi.md#clusters_get) | **GET** /clusters | Retrieve all Clusters
[**clusters_post**](ClustersApi.md#clusters_post) | **POST** /clusters | Create Cluster


# **clusters_delete**
> clusters_delete(cluster_id)

Delete Cluster

Deletes the specified Cluster.

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
    api_instance = ionoscloud_kafka.ClustersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.

    try:
        # Delete Cluster
        api_instance.clusters_delete(cluster_id)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 

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
**202** | Deleting Cluster was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_find_by_id**
> ClusterRead clusters_find_by_id(cluster_id)

Retrieve Cluster

Returns the Cluster by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.cluster_read import ClusterRead
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
    api_instance = ionoscloud_kafka.ClustersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.

    try:
        # Retrieve Cluster
        api_response = api_instance.clusters_find_by_id(cluster_id)
        print("The response of ClustersApi->clusters_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 

### Return type

[**ClusterRead**](ClusterRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting Cluster was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_get**
> ClusterReadList clusters_get(filter_name=filter_name, filter_state=filter_state)

Retrieve all Clusters

This endpoint enables retrieving all Clusters using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.cluster_read_list import ClusterReadList
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
    api_instance = ionoscloud_kafka.ClustersApi(api_client)
    filter_name = 'filter_name_example' # str | Only return Kafka clusters that contain the given name. Case insensitive. (optional)
    filter_state = 'filter_state_example' # str | Only return Kafka clusters with a given state. (optional)

    try:
        # Retrieve all Clusters
        api_response = api_instance.clusters_get(filter_name=filter_name, filter_state=filter_state)
        print("The response of ClustersApi->clusters_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_name** | **str**| Only return Kafka clusters that contain the given name. Case insensitive. | [optional] 
 **filter_state** | **str**| Only return Kafka clusters with a given state. | [optional] 

### Return type

[**ClusterReadList**](ClusterReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Clusters successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_post**
> ClusterRead clusters_post(cluster_create)

Create Cluster

Creates a new Cluster.

The full Cluster needs to be provided to create the object.
Optional data will be filled with defaults or left empty.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.cluster_create import ClusterCreate
from ionoscloud_kafka.models.cluster_read import ClusterRead
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
    api_instance = ionoscloud_kafka.ClustersApi(api_client)
    cluster_create = ionoscloud_kafka.ClusterCreate() # ClusterCreate | Cluster to create.

    try:
        # Create Cluster
        api_response = api_instance.clusters_post(cluster_create)
        print("The response of ClustersApi->clusters_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_create** | [**ClusterCreate**](ClusterCreate.md)| Cluster to create. | 

### Return type

[**ClusterRead**](ClusterRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Cluster successfully created. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

