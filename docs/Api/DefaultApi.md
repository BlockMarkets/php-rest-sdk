# BlockMarkets\DefaultApi

All URIs are relative to *https://api.blockmarkets.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**benchmarkRate**](DefaultApi.md#benchmarkRate) | **GET** /v1/rates/benchmark/{symbol} | Returns the latest available benchmark rates for a specific asset.
[**benchmarkRateHistory**](DefaultApi.md#benchmarkRateHistory) | **GET** /v1/rates/benchmark/{symbol}/history | Returns historical benchmark rates for an asset. Requires premium subscription.
[**listAssetMarkets**](DefaultApi.md#listAssetMarkets) | **GET** /v1/assets/{symbol} | Returns a list of all markets (base and quote) for a specific asset.
[**listAssets**](DefaultApi.md#listAssets) | **GET** /v1/assets | Returns a list of supported assets.
[**listBenchmarkRates**](DefaultApi.md#listBenchmarkRates) | **GET** /v1/rates/benchmark | Returns a list of supported USD benchmark rates.
[**listExchangeMarkets**](DefaultApi.md#listExchangeMarkets) | **GET** /v1/exchanges/{exchange} | Returns a list of markets for a specific exchange.
[**listExchanges**](DefaultApi.md#listExchanges) | **GET** /v1/exchanges | Returns a list of supported exchanges.
[**listMarkets**](DefaultApi.md#listMarkets) | **GET** /v1/markets | Returns a list of supported markets.
[**listPairMarkets**](DefaultApi.md#listPairMarkets) | **GET** /v1/pairs/{pair} | Returns a list of markets for a specific asset pair.
[**listPairs**](DefaultApi.md#listPairs) | **GET** /v1/pairs | Returns a list of supported asset pairs.
[**listSpotRates**](DefaultApi.md#listSpotRates) | **GET** /v1/rates/spot | Returns a list of supported USD spot rates.
[**marketBook**](DefaultApi.md#marketBook) | **GET** /v1/markets/{exchange}/{pair}/book | Returns the top 50 bids and asks from the current order book for a market pair. Requires premium subscription.
[**marketOHLCV**](DefaultApi.md#marketOHLCV) | **GET** /v1/markets/{exchange}/{pair}/ohlcv | Returns OHLCV history for a market pair.
[**marketTicker**](DefaultApi.md#marketTicker) | **GET** /v1/markets/{exchange}/{pair} | Returns the latest ticker for a market pair.
[**marketTrades**](DefaultApi.md#marketTrades) | **GET** /v1/markets/{exchange}/{pair}/trades | Returns trades for a market pair. Requires premium subscription.
[**spotRate**](DefaultApi.md#spotRate) | **GET** /v1/rates/spot/{symbol} | Returns the last USD spot rate for an asset.
[**spotRateHistory**](DefaultApi.md#spotRateHistory) | **GET** /v1/rates/spot/{symbol}/history | Returns historical spot rates for an asset. Requires premium subscription.
[**spotRateOHLCV**](DefaultApi.md#spotRateOHLCV) | **GET** /v1/rates/spot/{symbol}/ohlcv | Returns the OHLCV history for a spot rate.


# **benchmarkRate**
> \BlockMarkets\Model\ModelEmpty benchmarkRate($symbol)

Returns the latest available benchmark rates for a specific asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)

try {
    $result = $apiInstance->benchmarkRate($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->benchmarkRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **benchmarkRateHistory**
> \BlockMarkets\Model\ModelEmpty benchmarkRateHistory($symbol, $close)

Returns historical benchmark rates for an asset. Requires premium subscription.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)
$close = 'close_example'; // string | The closing time. Options - 4pm-gmt-close, 4pm-est-close, 0-utc-close

try {
    $result = $apiInstance->benchmarkRateHistory($symbol, $close);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->benchmarkRateHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |
 **close** | **string**| The closing time. Options - 4pm-gmt-close, 4pm-est-close, 0-utc-close | [optional]

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAssetMarkets**
> \BlockMarkets\Model\ModelEmpty listAssetMarkets($symbol)

Returns a list of all markets (base and quote) for a specific asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)

try {
    $result = $apiInstance->listAssetMarkets($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listAssetMarkets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAssets**
> \BlockMarkets\Model\ModelEmpty listAssets()

Returns a list of supported assets.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listAssets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listAssets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listBenchmarkRates**
> \BlockMarkets\Model\ModelEmpty listBenchmarkRates()

Returns a list of supported USD benchmark rates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listBenchmarkRates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listBenchmarkRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listExchangeMarkets**
> \BlockMarkets\Model\ModelEmpty listExchangeMarkets($exchange)

Returns a list of markets for a specific exchange.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$exchange = 'exchange_example'; // string | The 4-char exchange code (see /exchanges)

try {
    $result = $apiInstance->listExchangeMarkets($exchange);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listExchangeMarkets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exchange** | **string**| The 4-char exchange code (see /exchanges) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listExchanges**
> \BlockMarkets\Model\ModelEmpty listExchanges()

Returns a list of supported exchanges.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listExchanges();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listExchanges: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listMarkets**
> \BlockMarkets\Model\ModelEmpty listMarkets()

Returns a list of supported markets.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listMarkets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listPairMarkets**
> \BlockMarkets\Model\ModelEmpty listPairMarkets($pair)

Returns a list of markets for a specific asset pair.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pair = 'pair_example'; // string | The asset pair (see /pairs)

try {
    $result = $apiInstance->listPairMarkets($pair);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listPairMarkets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pair** | **string**| The asset pair (see /pairs) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listPairs**
> \BlockMarkets\Model\ModelEmpty listPairs()

Returns a list of supported asset pairs.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listPairs();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listPairs: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listSpotRates**
> \BlockMarkets\Model\ModelEmpty listSpotRates()

Returns a list of supported USD spot rates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listSpotRates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->listSpotRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **marketBook**
> \BlockMarkets\Model\ModelEmpty marketBook($exchange, $pair)

Returns the top 50 bids and asks from the current order book for a market pair. Requires premium subscription.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$exchange = 'exchange_example'; // string | The 4-char exchange code (see /exchanges)
$pair = 'pair_example'; // string | The asset pair (see /pairs)

try {
    $result = $apiInstance->marketBook($exchange, $pair);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->marketBook: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exchange** | **string**| The 4-char exchange code (see /exchanges) |
 **pair** | **string**| The asset pair (see /pairs) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **marketOHLCV**
> \BlockMarkets\Model\ModelEmpty marketOHLCV($exchange, $pair, $limit, $interval, $start, $end)

Returns OHLCV history for a market pair.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$exchange = 'exchange_example'; // string | The 4-char exchange code (see /exchanges)
$pair = 'pair_example'; // string | The asset pair (see /pairs)
$limit = 56; // int | Number of records to retrieve (default=100, max=1000)
$interval = 56; // int | Interval period in minutes. Supported - 1,3,5,15,30,60,1440 (default=1440)
$start = 'start_example'; // string | Start datetime in ISO 8601
$end = 'end_example'; // string | End datetime in ISO 8601

try {
    $result = $apiInstance->marketOHLCV($exchange, $pair, $limit, $interval, $start, $end);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->marketOHLCV: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exchange** | **string**| The 4-char exchange code (see /exchanges) |
 **pair** | **string**| The asset pair (see /pairs) |
 **limit** | **int**| Number of records to retrieve (default&#x3D;100, max&#x3D;1000) | [optional]
 **interval** | **int**| Interval period in minutes. Supported - 1,3,5,15,30,60,1440 (default&#x3D;1440) | [optional]
 **start** | **string**| Start datetime in ISO 8601 | [optional]
 **end** | **string**| End datetime in ISO 8601 | [optional]

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **marketTicker**
> \BlockMarkets\Model\ModelEmpty marketTicker($exchange, $pair)

Returns the latest ticker for a market pair.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$exchange = 'exchange_example'; // string | The 4-char exchange code (see /exchanges)
$pair = 'pair_example'; // string | The asset pair (see /pairs)

try {
    $result = $apiInstance->marketTicker($exchange, $pair);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->marketTicker: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exchange** | **string**| The 4-char exchange code (see /exchanges) |
 **pair** | **string**| The asset pair (see /pairs) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **marketTrades**
> \BlockMarkets\Model\ModelEmpty marketTrades($exchange, $pair, $limit, $start, $end)

Returns trades for a market pair. Requires premium subscription.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$exchange = 'exchange_example'; // string | The 4-char exchange code (see /exchanges)
$pair = 'pair_example'; // string | The asset pair (see /pairs)
$limit = 56; // int | Number of records to retrieve (default=100, max=1000)
$start = 'start_example'; // string | Start datetime in ISO 8601
$end = 'end_example'; // string | End datetime in ISO 8601

try {
    $result = $apiInstance->marketTrades($exchange, $pair, $limit, $start, $end);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->marketTrades: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exchange** | **string**| The 4-char exchange code (see /exchanges) |
 **pair** | **string**| The asset pair (see /pairs) |
 **limit** | **int**| Number of records to retrieve (default&#x3D;100, max&#x3D;1000) | [optional]
 **start** | **string**| Start datetime in ISO 8601 | [optional]
 **end** | **string**| End datetime in ISO 8601 | [optional]

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **spotRate**
> \BlockMarkets\Model\ModelEmpty spotRate($symbol)

Returns the last USD spot rate for an asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)

try {
    $result = $apiInstance->spotRate($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->spotRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **spotRateHistory**
> \BlockMarkets\Model\ModelEmpty spotRateHistory($symbol, $limit, $start, $end)

Returns historical spot rates for an asset. Requires premium subscription.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)
$limit = 56; // int | Number of records to retrieve (default=100, max=1000)
$start = 'start_example'; // string | Start datetime in ISO 8601
$end = 'end_example'; // string | End datetime in ISO 8601

try {
    $result = $apiInstance->spotRateHistory($symbol, $limit, $start, $end);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->spotRateHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |
 **limit** | **int**| Number of records to retrieve (default&#x3D;100, max&#x3D;1000) | [optional]
 **start** | **string**| Start datetime in ISO 8601 | [optional]
 **end** | **string**| End datetime in ISO 8601 | [optional]

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **spotRateOHLCV**
> \BlockMarkets\Model\ModelEmpty spotRateOHLCV($symbol, $limit, $interval, $start, $end)

Returns the OHLCV history for a spot rate.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BlockMarkets\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new BlockMarkets\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = 'symbol_example'; // string | The asset symbol (see /assets)
$limit = 56; // int | Number of records to retrieve (default=100, max=1000)
$interval = 56; // int | Interval period in minutes. Supported -  1,3,5,15,30,60,1440 (default=1440)
$start = 'start_example'; // string | Start datetime in ISO 8601
$end = 'end_example'; // string | End datetime in ISO 8601

try {
    $result = $apiInstance->spotRateOHLCV($symbol, $limit, $interval, $start, $end);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->spotRateOHLCV: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The asset symbol (see /assets) |
 **limit** | **int**| Number of records to retrieve (default&#x3D;100, max&#x3D;1000) | [optional]
 **interval** | **int**| Interval period in minutes. Supported -  1,3,5,15,30,60,1440 (default&#x3D;1440) | [optional]
 **start** | **string**| Start datetime in ISO 8601 | [optional]
 **end** | **string**| End datetime in ISO 8601 | [optional]

### Return type

[**\BlockMarkets\Model\ModelEmpty**](../Model/ModelEmpty.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

