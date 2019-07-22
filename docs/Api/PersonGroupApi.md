# Swagger\Client\PersonGroupApi

All URIs are relative to *https://face.himni.com.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**personGroupCreate**](PersonGroupApi.md#persongroupcreate) | **POST** /person-groups | Person Group - Create
[**personGroupDelete**](PersonGroupApi.md#persongroupdelete) | **DELETE** /person-groups/{person_group_uuid} | Person Group - Delete
[**personGroupList**](PersonGroupApi.md#persongrouplist) | **GET** /person-groups | Person Group - List
[**personGroupUpdate**](PersonGroupApi.md#persongroupupdate) | **PATCH** /person-groups/{person_group_uuid} | Person Group - Update
[**personGroupView**](PersonGroupApi.md#persongroupview) | **GET** /person-groups/{person_group_uuid} | Person Group - View

# **personGroupCreate**
> \Swagger\Client\Model\PersonGroupCreate personGroupCreate($body)

Person Group - Create

Cria um novo grupo de pessoas com nome e metadados especificados pelo usuário.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonGroupCreateRequest(); // \Swagger\Client\Model\PersonGroupCreateRequest | 

try {
    $result = $apiInstance->personGroupCreate($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonGroupApi->personGroupCreate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonGroupCreateRequest**](../Model/PersonGroupCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\PersonGroupCreate**](../Model/PersonGroupCreate.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personGroupDelete**
> personGroupDelete($person_group_uuid)

Person Group - Delete

Exclui um grupo de pessoas existente. Todos as informações persistidas neste grupo de pessoas, incluindo as pessoas e os modelos de reconhecimento facial serão excluídos.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_group_uuid = "person_group_uuid_example"; // string | 

try {
    $apiInstance->personGroupDelete($person_group_uuid);
} catch (Exception $e) {
    echo 'Exception when calling PersonGroupApi->personGroupDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_group_uuid** | **string**|  |

### Return type

void (empty response body)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personGroupList**
> \Swagger\Client\Model\PersonGroupsList[] personGroupList()

Person Group - List

Retorna uma listagem de todos os grupos de pessoas existentes contendo UUID, nome, metadados e quantidade de entidades cadastradas.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->personGroupList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonGroupApi->personGroupList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\PersonGroupsList[]**](../Model/PersonGroupsList.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personGroupUpdate**
> \Swagger\Client\Model\PersonGroupUpdate personGroupUpdate($body, $person_group_uuid)

Person Group - Update

Atualiza o nome e metadados de um grupo de pessoas existente. As propriedades que estiverem ausentes do corpo da requisição não serão alteradas.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonGroupUpdateRequest(); // \Swagger\Client\Model\PersonGroupUpdateRequest | 
$person_group_uuid = "person_group_uuid_example"; // string | 

try {
    $result = $apiInstance->personGroupUpdate($body, $person_group_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonGroupApi->personGroupUpdate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonGroupUpdateRequest**](../Model/PersonGroupUpdateRequest.md)|  |
 **person_group_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonGroupUpdate**](../Model/PersonGroupUpdate.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personGroupView**
> \Swagger\Client\Model\PersonGroupsView personGroupView($person_group_uuid)

Person Group - View

Retorna as informações de um grupo de pessoas, incluindo nome, metadados, UUID e quantidade de entidades cadastradas. Este endpoint retorna apenas os dados do grupo de pessoas, para obter a lista de pessoas neste grupo utilize o endpoint Person - List.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\PersonGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_group_uuid = "person_group_uuid_example"; // string | 

try {
    $result = $apiInstance->personGroupView($person_group_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonGroupApi->personGroupView: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_group_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonGroupsView**](../Model/PersonGroupsView.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

