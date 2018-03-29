# Telstra_EventDetection::RegistrationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**register**](RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
[**unregister**](RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


# **register**
> ResisterPhoneNumberList register(body)

Register

Register for an event

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'
# setup authorization
Telstra_EventDetection.configure do |config|
  # Configure OAuth2 access token for authorization: auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = Telstra_EventDetection::RegistrationApi.new

body = Telstra_EventDetection::SubscriptionObj.new # SubscriptionObj | Subscribe with a list of phone numbers, push notification URL (optional) and the event type.


begin
  #Register
  result = api_instance.register(body)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling RegistrationApi->register: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubscriptionObj**](SubscriptionObj.md)| Subscribe with a list of phone numbers, push notification URL (optional) and the event type. | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **unregister**
> ResisterPhoneNumberList unregister(event_type, body)

Unregister

Unregister from an event

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'
# setup authorization
Telstra_EventDetection.configure do |config|
  # Configure OAuth2 access token for authorization: auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = Telstra_EventDetection::RegistrationApi.new

event_type = "event_type_example" # String | Event Type

body = Telstra_EventDetection::UnregisterRequestObj.new # UnregisterRequestObj | List of subscribed phone numbers and notification URL (optional)


begin
  #Unregister
  result = api_instance.unregister(event_type, body)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling RegistrationApi->unregister: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_type** | **String**| Event Type | 
 **body** | [**UnregisterRequestObj**](UnregisterRequestObj.md)| List of subscribed phone numbers and notification URL (optional) | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



