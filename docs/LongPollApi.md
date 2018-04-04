# Telstra_EventDetection::LongPollApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**longpoll**](LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events


# **longpoll**
> GetEventResponse longpoll(event_type, body)

Poll events

Poll events for a given set of MSISDNs

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'
# setup authorization
Telstra_EventDetection.configure do |config|
  # Configure OAuth2 access token for authorization: auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = Telstra_EventDetection::LongPollApi.new

event_type = "event_type_example" # String | Event Type

body = Telstra_EventDetection::PollingObj.new # PollingObj | List of MSISDNs to pull the events


begin
  #Poll events
  result = api_instance.longpoll(event_type, body)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling LongPollApi->longpoll: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_type** | **String**| Event Type | 
 **body** | [**PollingObj**](PollingObj.md)| List of MSISDNs to pull the events | 

### Return type

[**GetEventResponse**](GetEventResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



