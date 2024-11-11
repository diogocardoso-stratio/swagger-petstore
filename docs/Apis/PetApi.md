# PetApi

All URIs are relative to */v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addPet**](PetApi.md#addPet) | **POST** /pet | Add a new pet to the store |
| [**deletePet**](PetApi.md#deletePet) | **DELETE** /pet/{petId} | Deletes a pet |
| [**findPetsByStatus**](PetApi.md#findPetsByStatus) | **GET** /pet/findByStatus | Finds Pets by status |
| [**findPetsByTags**](PetApi.md#findPetsByTags) | **GET** /pet/findByTags | Finds Pets by tags |
| [**getPetById**](PetApi.md#getPetById) | **GET** /pet/{petId} | Find pet by ID |
| [**updatePet**](PetApi.md#updatePet) | **PUT** /pet | Update an existing pet |
| [**updatePetWithForm**](PetApi.md#updatePetWithForm) | **POST** /pet/{petId} | Updates a pet in the store with form data |
| [**uploadFile**](PetApi.md#uploadFile) | **POST** /pet/{petId}/uploadImage | uploads an image |


<a name="addPet"></a>
# **addPet**
> Pet addPet(Pet)

Add a new pet to the store

    Add a new pet to the store

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **Pet** | [**Pet**](../Models/Pet.md)| Create a new pet in the store | |

### Return type

[**Pet**](../Models/Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
- **Accept**: application/xml, application/json

<a name="deletePet"></a>
# **deletePet**
> deletePet(petId, api\_key)

Deletes a pet

    

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **petId** | **Long**| Pet id to delete | [default to null] |
| **api\_key** | **String**|  | [optional] [default to null] |

### Return type

null (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="findPetsByStatus"></a>
# **findPetsByStatus**
> List findPetsByStatus(status)

Finds Pets by status

    Multiple status values can be provided with comma separated strings

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **status** | **String**| Status values that need to be considered for filter | [optional] [default to available] [enum: available, pending, sold] |

### Return type

[**List**](../Models/Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json

<a name="findPetsByTags"></a>
# **findPetsByTags**
> List findPetsByTags(tags)

Finds Pets by tags

    Multiple tags can be provided with comma separated strings. Use tag1, tag2, tag3 for testing.

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **tags** | [**List**](../Models/String.md)| Tags to filter by | [optional] [default to null] |

### Return type

[**List**](../Models/Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json

<a name="getPetById"></a>
# **getPetById**
> Pet getPetById(petId)

Find pet by ID

    Returns a single pet

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **petId** | **Long**| ID of pet to return | [default to null] |

### Return type

[**Pet**](../Models/Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth), [api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json

<iframe src="https://petstore.swagger.io/?url=https://raw.githubusercontent.com/diogocardoso-stratio/swagger-petstore/master/src/main/resources/openapi.yaml#/pet/{petId}" width="100%" height="400px"></iframe>

<a name="updatePet"></a>
# **updatePet**
> Pet updatePet(Pet)

Update an existing pet

    Update an existing pet by Id

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **Pet** | [**Pet**](../Models/Pet.md)| Update an existent pet in the store | |

### Return type

[**Pet**](../Models/Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
- **Accept**: application/xml, application/json

<a name="updatePetWithForm"></a>
# **updatePetWithForm**
> updatePetWithForm(petId, name, status)

Updates a pet in the store with form data

    

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **petId** | **Long**| ID of pet that needs to be updated | [default to null] |
| **name** | **String**| Name of pet that needs to be updated | [optional] [default to null] |
| **status** | **String**| Status of pet that needs to be updated | [optional] [default to null] |

### Return type

null (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="uploadFile"></a>
# **uploadFile**
> ApiResponse uploadFile(petId, additionalMetadata, body)

uploads an image

    

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **petId** | **Long**| ID of pet to update | [default to null] |
| **additionalMetadata** | **String**| Additional Metadata | [optional] [default to null] |
| **body** | **File**|  | [optional] |

### Return type

[**ApiResponse**](../Models/ApiResponse.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

