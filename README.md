# Telstra_EventDetection

Telstra_EventDetection - the Ruby gem for the Telstra Event Detection API

- API version: 1.0.0
- Package version: 1.0.0

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build Telstra_EventDetection.gemspec
```

Then either install the gem locally:

```shell
gem install ./Telstra_EventDetection-1.0.0.gem
```
(for development, run `gem install --dev ./Telstra_EventDetection-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'Telstra_EventDetection', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/Telstra/EventDetectionAPI-SDK-ruby, then add the following in the Gemfile:

    gem 'Telstra_EventDetection', :git => 'https://github.com/Telstra/EventDetectionAPI-SDK-ruby.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:
```ruby
# Load the gem
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

## Documentation for API Endpoints

All URIs are relative to *https://tapi.telstra.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Telstra_EventDetection::AuthenticationApi* | [**auth_token**](docs/AuthenticationApi.md#auth_token) | **POST** /v2/oauth/token | Generate authentication token
*Telstra_EventDetection::GetSubscriptionApi* | [**get_subscription**](docs/GetSubscriptionApi.md#get_subscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions
*Telstra_EventDetection::LongPollApi* | [**longpoll**](docs/LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events
*Telstra_EventDetection::PushNotificationsApi* | [**push_notifications**](docs/PushNotificationsApi.md#push_notifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications
*Telstra_EventDetection::RegistrationApi* | [**register**](docs/RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
*Telstra_EventDetection::RegistrationApi* | [**unregister**](docs/RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


## Documentation for Models

 - [Telstra_EventDetection::Eventsattr](docs/Eventsattr.md)
 - [Telstra_EventDetection::GetEventResponse](docs/GetEventResponse.md)
 - [Telstra_EventDetection::GetSubscriptionResponse](docs/GetSubscriptionResponse.md)
 - [Telstra_EventDetection::NotificationPayload](docs/NotificationPayload.md)
 - [Telstra_EventDetection::OAuthResponse](docs/OAuthResponse.md)
 - [Telstra_EventDetection::PhoneNumberList](docs/PhoneNumberList.md)
 - [Telstra_EventDetection::PollingObj](docs/PollingObj.md)
 - [Telstra_EventDetection::PushNotificationObj](docs/PushNotificationObj.md)
 - [Telstra_EventDetection::ResisterPhoneNumberList](docs/ResisterPhoneNumberList.md)
 - [Telstra_EventDetection::ServiceEventsAttr](docs/ServiceEventsAttr.md)
 - [Telstra_EventDetection::SubscriptionObj](docs/SubscriptionObj.md)
 - [Telstra_EventDetection::Subscriptionattr](docs/Subscriptionattr.md)
 - [Telstra_EventDetection::Test](docs/Test.md)
 - [Telstra_EventDetection::UnregisterRequestObj](docs/UnregisterRequestObj.md)


## Documentation for Authorisation


### auth

- **Type**: OAuth
- **Flow**: application
- **Authorisation URL**: 
- **Scopes**: 
  - v1_eventdetection_simswap: v1_eventdetection_simswap

