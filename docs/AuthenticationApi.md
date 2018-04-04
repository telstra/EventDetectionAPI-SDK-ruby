# Telstra_EventDetection::AuthenticationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auth_token**](AuthenticationApi.md#auth_token) | **POST** /v2/oauth/token | Generate authentication token


# **auth_token**
> OAuthResponse auth_token(client_id, client_secret, grant_type)

Generate authentication token

Generate authentication token

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'

api_instance = Telstra_EventDetection::AuthenticationApi.new

client_id = "client_id_example" # String | 

client_secret = "client_secret_example" # String | 

grant_type = "client_credentials" # String | 


begin
  #Generate authentication token
  result = api_instance.auth_token(client_id, client_secret, grant_type)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling AuthenticationApi->auth_token: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **String**|  | 
 **client_secret** | **String**|  | 
 **grant_type** | **String**|  | [default to client_credentials]

### Return type

[**OAuthResponse**](OAuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json



