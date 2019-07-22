# Swagger\Client\PersonApi

All URIs are relative to *https://face.himni.com.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**personCreate**](PersonApi.md#personcreate) | **POST** /persons | Person - Create
[**personDelete**](PersonApi.md#persondelete) | **DELETE** /persons/{person_uuid} | Person - Delete
[**personList**](PersonApi.md#personlist) | **GET** /persons | Person - List
[**personUpdate**](PersonApi.md#personupdate) | **PATCH** /persons/{person_uuid} | Person - Update
[**personView**](PersonApi.md#personview) | **GET** /persons/{person_uuid} | Person - View

# **personCreate**
> \Swagger\Client\Model\PersonCreate personCreate($body)

Person - Create

Cria uma nova Pessoa no Grupo de Pessoas especificado. Para cadastrar uma Face para esta Pessoa, utilize o endpoint Person - Create Face.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonCreateRequest(); // \Swagger\Client\Model\PersonCreateRequest | 

try {
    $result = $apiInstance->personCreate($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->personCreate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonCreateRequest**](../Model/PersonCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\PersonCreate**](../Model/PersonCreate.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personDelete**
> personDelete($person_uuid)

Person - Delete

Exclui uma Pessoa existente em um Grupo de Pessoas. Todos os dados relacionados a esta entidade (nome, metadados, identificador e modelos de reconhecimento facial) serão excluídos.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 

try {
    $apiInstance->personDelete($person_uuid);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->personDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |

### Return type

void (empty response body)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personList**
> \Swagger\Client\Model\PersonList[] personList()

Person - List

Exibe uma listagem de todas as informações das Pessoas no Grupo de Pessoas especificado, incluindo identificador, nome, metadados e modelos de reconhecimento facial cadastrados.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->personList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->personList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\PersonList[]**](../Model/PersonList.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personUpdate**
> \Swagger\Client\Model\PersonUpdate personUpdate($body, $person_uuid)

Person - Update

Atualiza o nome e / ou metadados de uma Pessoa.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonUpdateRequest(); // \Swagger\Client\Model\PersonUpdateRequest | 
$person_uuid = "person_uuid_example"; // string | 

try {
    $result = $apiInstance->personUpdate($body, $person_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->personUpdate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonUpdateRequest**](../Model/PersonUpdateRequest.md)|  |
 **person_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonUpdate**](../Model/PersonUpdate.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personView**
> \Swagger\Client\Model\PersonView personView($person_uuid)

Person - View

Retorna o nome, os metadados e os modelos de reconhecimento facial de uma Pessoa.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 

try {
    $result = $apiInstance->personView($person_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->personView: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonView**](../Model/PersonView.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

