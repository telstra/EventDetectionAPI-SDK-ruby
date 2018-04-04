# Telstra_EventDetection::PushNotificationsApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**push_notifications**](PushNotificationsApi.md#push_notifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications


# **push_notifications**
> PushNotificationObj push_notifications(content_type, body)

Push event notifications

Push event notifications to the notification URL configured during the MSISDN registration process

### Example
```ruby
# load the gem
require 'Telstra_EventDetection'

api_instance = Telstra_EventDetection::PushNotificationsApi.new

content_type = "content_type_example" # String | application/json

body = Telstra_EventDetection::NotificationPayload.new # NotificationPayload | Application Id, MSISDN, Event Id and Event Date


begin
  #Push event notifications
  result = api_instance.push_notifications(content_type, body)
  p result
rescue Telstra_EventDetection::ApiError => e
  puts "Exception when calling PushNotificationsApi->push_notifications: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **content_type** | **String**| application/json | 
 **body** | [**NotificationPayload**](NotificationPayload.md)| Application Id, MSISDN, Event Id and Event Date | 

### Return type

[**PushNotificationObj**](PushNotificationObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



