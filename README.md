# pet_store_client

PetStoreClient - the Ruby gem for the OpenAPI Petstore

This is a sample server Petstore server. For this sample, you can use the api key `special-key` to test the authorization filters.

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build pet_store_client.gemspec
```

Then either install the gem locally:

```shell
gem install ./pet_store_client-1.0.0.gem
```

(for development, run `gem install --dev ./pet_store_client-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'pet_store_client', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/GIT_USER_ID/GIT_REPO_ID, then add the following in the Gemfile:

    gem 'pet_store_client', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
# Load the gem
require 'pet_store_client'

# Setup authorization
PetStoreClient.configure do |config|
  # Configure OAuth2 access token for authorization: petstore_auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = PetStoreClient::PetApi.new
pet = PetStoreClient::Pet.new # Pet | Pet object that needs to be added to the store

begin
  #Add a new pet to the store
  result = api_instance.add_pet(pet)
  p result
rescue PetStoreClient::ApiError => e
  puts "Exception when calling PetApi->add_pet: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *http://petstore.swagger.io/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*PetStoreClient::PetApi* | [**add_pet**](docs/PetApi.md#add_pet) | **POST** /pet | Add a new pet to the store
*PetStoreClient::PetApi* | [**delete_pet**](docs/PetApi.md#delete_pet) | **DELETE** /pet/{petId} | Deletes a pet
*PetStoreClient::PetApi* | [**find_pets_by_status**](docs/PetApi.md#find_pets_by_status) | **GET** /pet/findByStatus | Finds Pets by status
*PetStoreClient::PetApi* | [**find_pets_by_tags**](docs/PetApi.md#find_pets_by_tags) | **GET** /pet/findByTags | Finds Pets by tags
*PetStoreClient::PetApi* | [**get_pet_by_id**](docs/PetApi.md#get_pet_by_id) | **GET** /pet/{petId} | Find pet by ID
*PetStoreClient::PetApi* | [**update_pet**](docs/PetApi.md#update_pet) | **PUT** /pet | Update an existing pet
*PetStoreClient::PetApi* | [**update_pet_with_form**](docs/PetApi.md#update_pet_with_form) | **POST** /pet/{petId} | Updates a pet in the store with form data
*PetStoreClient::PetApi* | [**upload_file**](docs/PetApi.md#upload_file) | **POST** /pet/{petId}/uploadImage | uploads an image
*PetStoreClient::StoreApi* | [**delete_order**](docs/StoreApi.md#delete_order) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
*PetStoreClient::StoreApi* | [**get_inventory**](docs/StoreApi.md#get_inventory) | **GET** /store/inventory | Returns pet inventories by status
*PetStoreClient::StoreApi* | [**get_order_by_id**](docs/StoreApi.md#get_order_by_id) | **GET** /store/order/{orderId} | Find purchase order by ID
*PetStoreClient::StoreApi* | [**place_order**](docs/StoreApi.md#place_order) | **POST** /store/order | Place an order for a pet
*PetStoreClient::UserApi* | [**create_user**](docs/UserApi.md#create_user) | **POST** /user | Create user
*PetStoreClient::UserApi* | [**create_users_with_array_input**](docs/UserApi.md#create_users_with_array_input) | **POST** /user/createWithArray | Creates list of users with given input array
*PetStoreClient::UserApi* | [**create_users_with_list_input**](docs/UserApi.md#create_users_with_list_input) | **POST** /user/createWithList | Creates list of users with given input array
*PetStoreClient::UserApi* | [**delete_user**](docs/UserApi.md#delete_user) | **DELETE** /user/{username} | Delete user
*PetStoreClient::UserApi* | [**get_user_by_name**](docs/UserApi.md#get_user_by_name) | **GET** /user/{username} | Get user by user name
*PetStoreClient::UserApi* | [**login_user**](docs/UserApi.md#login_user) | **GET** /user/login | Logs user into the system
*PetStoreClient::UserApi* | [**logout_user**](docs/UserApi.md#logout_user) | **GET** /user/logout | Logs out current logged in user session
*PetStoreClient::UserApi* | [**update_user**](docs/UserApi.md#update_user) | **PUT** /user/{username} | Updated user


## Documentation for Models

 - [PetStoreClient::ApiResponse](docs/ApiResponse.md)
 - [PetStoreClient::Category](docs/Category.md)
 - [PetStoreClient::InlineObject](docs/InlineObject.md)
 - [PetStoreClient::InlineObject1](docs/InlineObject1.md)
 - [PetStoreClient::Order](docs/Order.md)
 - [PetStoreClient::Pet](docs/Pet.md)
 - [PetStoreClient::Tag](docs/Tag.md)
 - [PetStoreClient::User](docs/User.md)


## Documentation for Authorization


### api_key


- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

### petstore_auth


- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: http://petstore.swagger.io/api/oauth/dialog
- **Scopes**: 
  - write:pets: modify pets in your account
  - read:pets: read your pets

