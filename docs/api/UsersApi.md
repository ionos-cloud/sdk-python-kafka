# ionoscloud_kafka.UsersApi

All URIs are relative to *https://kafka.de-fra.ionos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clusters_users_access_get**](UsersApi.md#clusters_users_access_get) | **GET** /clusters/{clusterId}/users/{userId}/access | Retrieve Apache Kafka User with Credentials
[**clusters_users_get**](UsersApi.md#clusters_users_get) | **GET** /clusters/{clusterId}/users | Retrieve all Users


# **clusters_users_access_get**
> UserReadAccess clusters_users_access_get(cluster_id, user_id)

Retrieve Apache Kafka User with Credentials

Returns the user by ID containing its access certificates in the metadata.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.user_read_access import UserReadAccess
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
    api_instance = ionoscloud_kafka.UsersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the cluster.
    user_id = 'd11db12c-2625-5664-afd4-a3599731b5af' # str | The ID (UUID) of the user.

    try:
        # Retrieve Apache Kafka User with Credentials
        api_response = api_instance.clusters_users_access_get(cluster_id, user_id)
        print("The response of UsersApi->clusters_users_access_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->clusters_users_access_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the cluster. | 
 **user_id** | **str**| The ID (UUID) of the user. | 

### Return type

[**UserReadAccess**](UserReadAccess.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get user access information was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_users_get**
> UserReadList clusters_users_get(cluster_id)

Retrieve all Users

This endpoint enables retrieving all Users using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_kafka
from ionoscloud_kafka.models.user_read_list import UserReadList
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
    api_instance = ionoscloud_kafka.UsersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.

    try:
        # Retrieve all Users
        api_response = api_instance.clusters_users_get(cluster_id)
        print("The response of UsersApi->clusters_users_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->clusters_users_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 

### Return type

[**UserReadList**](UserReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Users successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

