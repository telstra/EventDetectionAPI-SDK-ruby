# Telstra_EventDetection::GetSubscriptionApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_subscription**](GetSubscriptionApi.md#get_subscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions


# **get_subscription**
> GetSubscriptionResponse get_subscription(body)

Get Event Subscriptions

Get the list of events subscribed for

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'
# setup authorization
Telstra_EventDetection.configure do |config|
  # Configure OAuth2 access token for authorization: auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = Telstra_EventDetection::GetSubscriptionApi.new

body = Telstra_EventDetection::PhoneNumberList.new # PhoneNumberList | List of subscribed phone numbers


begin
  #Get Event Subscriptions
  result = api_instance.get_subscription(body)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling GetSubscriptionApi->get_subscription: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhoneNumberList**](PhoneNumberList.md)| List of subscribed phone numbers | 

### Return type

[**GetSubscriptionResponse**](GetSubscriptionResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



