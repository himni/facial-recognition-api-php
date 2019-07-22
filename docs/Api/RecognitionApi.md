# Swagger\Client\RecognitionApi

All URIs are relative to *https://face.himni.com.br*

Method | HTTP request | Description
------------- | ------------- | -------------
[**personGroupIdentify**](RecognitionApi.md#persongroupidentify) | **POST** /person-groups/{person_group_uuid}/identify | Person Group - Identify
[**personVerify**](RecognitionApi.md#personverify) | **POST** /persons/{person_uuid}/verify | Person - Verify

# **personGroupIdentify**
> \Swagger\Client\Model\PersonGroupIdentify[] personGroupIdentify($person_group_uuid, $picture)

Person Group - Identify

Identificação das correspondências mais próximas a uma imagem enviada, dentro de um Grupo de Pessoas. Será calculada a similaridade entre a imagem enviada e os modelos de reconhecimento facial cadastrados no Grupo de Pessoas, e será retornada uma listagem dos candidatos àquela Face ordenadas pelo índice de confiança.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\RecognitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_group_uuid = "person_group_uuid_example"; // string | 
$picture = "picture_example"; // string | 

try {
    $result = $apiInstance->personGroupIdentify($person_group_uuid, $picture);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecognitionApi->personGroupIdentify: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_group_uuid** | **string**|  |
 **picture** | **string****string**|  | [optional]

### Return type

[**\Swagger\Client\Model\PersonGroupIdentify[]**](../Model/PersonGroupIdentify.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **personVerify**
> \Swagger\Client\Model\PersonVerify personVerify($person_uuid, $picture)

Person - Verify

Verifica se a imagem enviada corresponde à uma Pessoa específica.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\RecognitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_uuid = "person_uuid_example"; // string | 
$picture = "picture_example"; // string | 

try {
    $result = $apiInstance->personVerify($person_uuid, $picture);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecognitionApi->personVerify: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_uuid** | **string**|  |
 **picture** | **string****string**|  | [optional]

### Return type

[**\Swagger\Client\Model\PersonVerify**](../Model/PersonVerify.md)

### Authorization

[httpBearer](../../README.md#httpBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

