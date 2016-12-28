# PaymentRails\Client\RecipientApi

All URIs are relative to *http://api.railz.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBankAccount**](RecipientApi.md#createBankAccount) | **POST** /v1/recipients/{recipientId}/payout-methods/accounts/bank | 
[**createPaypalAccount**](RecipientApi.md#createPaypalAccount) | **POST** /v1/recipients/{recipientId}/payout-methods/accounts/paypal | 
[**createRecipientPayoutMethods**](RecipientApi.md#createRecipientPayoutMethods) | **POST** /v1/recipients/{recipientId}/payout-methods | 
[**deleteRecipient**](RecipientApi.md#deleteRecipient) | **DELETE** /v1/recipients/{recipientId} | 
[**getBankAccount**](RecipientApi.md#getBankAccount) | **GET** /v1/recipients/{recipientId}/payout-methods/accounts/bank | 
[**getPaypalAccount**](RecipientApi.md#getPaypalAccount) | **GET** /v1/recipients/{recipientId}/payout-methods/accounts/paypal | 
[**getRecipient**](RecipientApi.md#getRecipient) | **GET** /v1/recipients/{recipientId} | 
[**getRecipientInfo**](RecipientApi.md#getRecipientInfo) | **GET** /v1/recipients/{recipientId}/info | 
[**getRecipientPayoutMethods**](RecipientApi.md#getRecipientPayoutMethods) | **GET** /v1/recipients/{recipientId}/payout-methods | 
[**queryRecipientComplianceHistory**](RecipientApi.md#queryRecipientComplianceHistory) | **GET** /v1/recipients/{recipientId}/compliance | 
[**queryRecipientLogHistory**](RecipientApi.md#queryRecipientLogHistory) | **GET** /v1/recipients/{recipientId}/logs | 
[**queryRecipientPaymentHistory**](RecipientApi.md#queryRecipientPaymentHistory) | **GET** /v1/recipients/{recipientId}/payments | 
[**updateBankAccount**](RecipientApi.md#updateBankAccount) | **PATCH** /v1/recipients/{recipientId}/payout-methods/accounts/bank | 
[**updatePaypalAccount**](RecipientApi.md#updatePaypalAccount) | **PATCH** /v1/recipients/{recipientId}/payout-methods/accounts/paypal | 
[**updateRecipient**](RecipientApi.md#updateRecipient) | **PATCH** /v1/recipients/{recipientId} | 
[**updateRecipientInfo**](RecipientApi.md#updateRecipientInfo) | **PATCH** /v1/recipients/{recipientId}/info | 
[**updateRecipientPayoutMethods**](RecipientApi.md#updateRecipientPayoutMethods) | **PATCH** /v1/recipients/{recipientId}/payout-methods | 


# **createBankAccount**
> \PaymentRails\Client\Model\BankAccount createBankAccount($recipient_id, $body)



create bank account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 
$body = new \PaymentRails\Client\Model\BankAccount(); // \PaymentRails\Client\Model\BankAccount | 

try {
    $result = $api_instance->createBankAccount($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->createBankAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |
 **body** | [**\PaymentRails\Client\Model\BankAccount**](../Model/\PaymentRails\Client\Model\BankAccount.md)|  |

### Return type

[**\PaymentRails\Client\Model\BankAccount**](../Model/BankAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createPaypalAccount**
> \PaymentRails\Client\Model\PaypalAccount createPaypalAccount($recipient_id, $body)



create paypal account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 
$body = new \PaymentRails\Client\Model\PaypalAccount(); // \PaymentRails\Client\Model\PaypalAccount | paypal payout account

try {
    $result = $api_instance->createPaypalAccount($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->createPaypalAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |
 **body** | [**\PaymentRails\Client\Model\PaypalAccount**](../Model/\PaymentRails\Client\Model\PaypalAccount.md)| paypal payout account |

### Return type

[**\PaymentRails\Client\Model\PaypalAccount**](../Model/PaypalAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createRecipientPayoutMethods**
> \PaymentRails\Client\Model\RecipientPayoutMethods createRecipientPayoutMethods($recipient_id, $body)



create recipient payout methods

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX
$body = new \PaymentRails\Client\Model\RecipientPayoutMethods(); // \PaymentRails\Client\Model\RecipientPayoutMethods | 

try {
    $result = $api_instance->createRecipientPayoutMethods($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->createRecipientPayoutMethods: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |
 **body** | [**\PaymentRails\Client\Model\RecipientPayoutMethods**](../Model/\PaymentRails\Client\Model\RecipientPayoutMethods.md)|  |

### Return type

[**\PaymentRails\Client\Model\RecipientPayoutMethods**](../Model/RecipientPayoutMethods.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteRecipient**
> deleteRecipient($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX

try {
    $api_instance->deleteRecipient($recipient_id);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->deleteRecipient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |

### Return type

void (empty response body)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBankAccount**
> \PaymentRails\Client\Model\BankAccount getBankAccount($recipient_id)



create bank account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 

try {
    $result = $api_instance->getBankAccount($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->getBankAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |

### Return type

[**\PaymentRails\Client\Model\BankAccount**](../Model/BankAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPaypalAccount**
> \PaymentRails\Client\Model\PaypalAccount getPaypalAccount($recipient_id)



get paypal account for recipient

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 

try {
    $result = $api_instance->getPaypalAccount($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->getPaypalAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |

### Return type

[**\PaymentRails\Client\Model\PaypalAccount**](../Model/PaypalAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecipient**
> \PaymentRails\Client\Model\Recipient getRecipient($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX

try {
    $result = $api_instance->getRecipient($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->getRecipient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |

### Return type

[**\PaymentRails\Client\Model\Recipient**](../Model/Recipient.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecipientInfo**
> \PaymentRails\Client\Model\RecipientInfoOut getRecipientInfo($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX

try {
    $result = $api_instance->getRecipientInfo($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->getRecipientInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |

### Return type

[**\PaymentRails\Client\Model\RecipientInfoOut**](../Model/RecipientInfoOut.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecipientPayoutMethods**
> \PaymentRails\Client\Model\RecipientPayoutMethods getRecipientPayoutMethods($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX

try {
    $result = $api_instance->getRecipientPayoutMethods($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->getRecipientPayoutMethods: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |

### Return type

[**\PaymentRails\Client\Model\RecipientPayoutMethods**](../Model/RecipientPayoutMethods.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryRecipientComplianceHistory**
> \PaymentRails\Client\Model\InlineResponse2002 queryRecipientComplianceHistory($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 

try {
    $result = $api_instance->queryRecipientComplianceHistory($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->queryRecipientComplianceHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |

### Return type

[**\PaymentRails\Client\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryRecipientLogHistory**
> \PaymentRails\Client\Model\InlineResponse2003 queryRecipientLogHistory($recipient_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXX

try {
    $result = $api_instance->queryRecipientLogHistory($recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->queryRecipientLogHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXX |

### Return type

[**\PaymentRails\Client\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryRecipientPaymentHistory**
> \PaymentRails\Client\Model\InlineResponse2004 queryRecipientPaymentHistory($recipient_id, $page, $page_size, $status, $start_date, $end_date, $source_currency, $search)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX
$page = 56; // int | set page number default 1
$page_size = 56; // int | set page size default 100
$status = "status_example"; // string | filter recipient payment by status
$start_date = "start_date_example"; // string | filter recipient payment creation date from date
$end_date = "end_date_example"; // string | filter recipient payment creation date to date
$source_currency = "source_currency_example"; // string | filter recipient payments by source currency, 3 letters ISO code
$search = "search_example"; // string | search payments using key words, payment ids, names

try {
    $result = $api_instance->queryRecipientPaymentHistory($recipient_id, $page, $page_size, $status, $start_date, $end_date, $source_currency, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->queryRecipientPaymentHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |
 **page** | **int**| set page number default 1 | [optional]
 **page_size** | **int**| set page size default 100 | [optional]
 **status** | **string**| filter recipient payment by status | [optional]
 **start_date** | **string**| filter recipient payment creation date from date | [optional]
 **end_date** | **string**| filter recipient payment creation date to date | [optional]
 **source_currency** | **string**| filter recipient payments by source currency, 3 letters ISO code | [optional]
 **search** | **string**| search payments using key words, payment ids, names | [optional]

### Return type

[**\PaymentRails\Client\Model\InlineResponse2004**](../Model/InlineResponse2004.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateBankAccount**
> \PaymentRails\Client\Model\BankAccount updateBankAccount($recipient_id, $body)



create bank account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 
$body = new \PaymentRails\Client\Model\BankAccount(); // \PaymentRails\Client\Model\BankAccount | 

try {
    $result = $api_instance->updateBankAccount($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->updateBankAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |
 **body** | [**\PaymentRails\Client\Model\BankAccount**](../Model/\PaymentRails\Client\Model\BankAccount.md)|  |

### Return type

[**\PaymentRails\Client\Model\BankAccount**](../Model/BankAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updatePaypalAccount**
> \PaymentRails\Client\Model\PaypalAccount updatePaypalAccount($recipient_id, $body)



create paypal account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | 
$body = new \PaymentRails\Client\Model\PaypalAccount(); // \PaymentRails\Client\Model\PaypalAccount | paypal payout account

try {
    $result = $api_instance->updatePaypalAccount($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->updatePaypalAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**|  |
 **body** | [**\PaymentRails\Client\Model\PaypalAccount**](../Model/\PaymentRails\Client\Model\PaypalAccount.md)| paypal payout account |

### Return type

[**\PaymentRails\Client\Model\PaypalAccount**](../Model/PaypalAccount.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateRecipient**
> \PaymentRails\Client\Model\Recipient updateRecipient($recipient_id, $body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX
$body = new \PaymentRails\Client\Model\RecipientPost(); // \PaymentRails\Client\Model\RecipientPost | 

try {
    $result = $api_instance->updateRecipient($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->updateRecipient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |
 **body** | [**\PaymentRails\Client\Model\RecipientPost**](../Model/\PaymentRails\Client\Model\RecipientPost.md)|  |

### Return type

[**\PaymentRails\Client\Model\Recipient**](../Model/Recipient.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateRecipientInfo**
> \PaymentRails\Client\Model\RecipientInfoOut updateRecipientInfo($recipient_id, $body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX
$body = new \PaymentRails\Client\Model\RecipientInfoIn(); // \PaymentRails\Client\Model\RecipientInfoIn | 

try {
    $result = $api_instance->updateRecipientInfo($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->updateRecipientInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |
 **body** | [**\PaymentRails\Client\Model\RecipientInfoIn**](../Model/\PaymentRails\Client\Model\RecipientInfoIn.md)|  |

### Return type

[**\PaymentRails\Client\Model\RecipientInfoOut**](../Model/RecipientInfoOut.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateRecipientPayoutMethods**
> \PaymentRails\Client\Model\RecipientPayoutMethods updateRecipientPayoutMethods($recipient_id, $body)



create recipient payout methods

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: merchantKey
PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// PaymentRails\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$api_instance = new PaymentRails\Client\Api\RecipientApi();
$recipient_id = "recipient_id_example"; // string | R-XXXXXXXXXXXXXXXX
$body = new \PaymentRails\Client\Model\RecipientPayoutMethods(); // \PaymentRails\Client\Model\RecipientPayoutMethods | 

try {
    $result = $api_instance->updateRecipientPayoutMethods($recipient_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipientApi->updateRecipientPayoutMethods: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient_id** | **string**| R-XXXXXXXXXXXXXXXX |
 **body** | [**\PaymentRails\Client\Model\RecipientPayoutMethods**](../Model/\PaymentRails\Client\Model\RecipientPayoutMethods.md)|  |

### Return type

[**\PaymentRails\Client\Model\RecipientPayoutMethods**](../Model/RecipientPayoutMethods.md)

### Authorization

[merchantKey](../../README.md#merchantKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)
