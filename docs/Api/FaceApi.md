# Swagger\Client\FaceApi

All URIs are relative to *https://face.himni.com.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**personCreateFace**](FaceApi.md#personcreateface) | **POST** /persons/{person_uuid} | Person - Create Face
[**personDeleteFace**](FaceApi.md#persondeleteface) | **DELETE** /persons/{person_uuid}/{face_uuid} | Person - Delete Face
[**personUpdateFace**](FaceApi.md#personupdateface) | **PATCH** /persons/{person_uuid}/{face_uuid} | Person - Update Face
[**personViewFace**](FaceApi.md#personviewface) | **GET** /persons/{person_uuid}/{face_uuid} | Person - View Face

# **personCreateFace**
> \Swagger\Client\Model\PersonCreateFace personCreateFace($person_uuid, $picture, $meta)

Person - Create Face

Cadastra uma Face para uma Pessoa no Grupo de Pessoas especificado. Em fotos com mais de um rosto, apenas o primeiro rosto identificado será utilizado. Nenhuma imagem é armazenada. Apenas os modelos de reconhecimento facial gerados a partir das imagens serão mantidos no servidor até que seja feita uma chamada a um destes endpoints: Person Group - Delete, Person - Delete e Person - Delete Face.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\FaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 
$picture = "picture_example"; // string | 
$meta = "meta_example"; // string | 

try {
    $result = $apiInstance->personCreateFace($person_uuid, $picture, $meta);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaceApi->personCreateFace: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |
 **picture** | **string****string**|  | [optional]
 **meta** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\PersonCreateFace**](../Model/PersonCreateFace.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personDeleteFace**
> personDeleteFace($person_uuid, $face_uuid)

Person - Delete Face

Exclui uma Face de uma Pessoa existente no Grupo de Pessoas especificado.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\FaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 
$face_uuid = "face_uuid_example"; // string | 

try {
    $apiInstance->personDeleteFace($person_uuid, $face_uuid);
} catch (Exception $e) {
    echo 'Exception when calling FaceApi->personDeleteFace: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |
 **face_uuid** | **string**|  |

### Return type

void (empty response body)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personUpdateFace**
> \Swagger\Client\Model\PersonUpdateFace personUpdateFace($body, $person_uuid, $face_uuid)

Person - Update Face

Atualiza os metados de uma Face existente.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\FaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonUpdateFaceRequest(); // \Swagger\Client\Model\PersonUpdateFaceRequest | 
$person_uuid = "person_uuid_example"; // string | 
$face_uuid = "face_uuid_example"; // string | 

try {
    $result = $apiInstance->personUpdateFace($body, $person_uuid, $face_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaceApi->personUpdateFace: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonUpdateFaceRequest**](../Model/PersonUpdateFaceRequest.md)|  |
 **person_uuid** | **string**|  |
 **face_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonUpdateFace**](../Model/PersonUpdateFace.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personViewFace**
> \Swagger\Client\Model\PersonViewFace personViewFace($person_uuid, $face_uuid)

Person - View Face

Exibe as informações (identificador e metadados) de uma Face.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\FaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 
$face_uuid = "face_uuid_example"; // string | 

try {
    $result = $apiInstance->personViewFace($person_uuid, $face_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaceApi->personViewFace: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |
 **face_uuid** | **string**|  |

### Return type

[**\Swagger\Client\Model\PersonViewFace**](../Model/PersonViewFace.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

