![banner](https://passbase-sdk-banner.netlify.app/php.png)

# Passbase PHP SDK

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.1.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 7.2 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/passbase/passbase-php.git"
    }
  ],
  "require": {
    "passbase/passbase-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/passbase/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Unique ID of the identity to return

try {
    $result = $apiInstance->getIdentityById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityById: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.passbase.com/verification/v1*

| Class         | Method                                                                                 | HTTP request                                                                     | Description          |
| ------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------- |
| _IdentityApi_ | [**getIdentityById**](docs/Api/IdentityApi.md#getidentitybyid)                         | **GET** /identities/{id}                                                         | Get identity         |
| _IdentityApi_ | [**getIdentityResourceById**](docs/Api/IdentityApi.md#getidentityresourcebyid)         | **GET** /identity/{id}/resources/{resource_id}                                   | Get resource         |
| _IdentityApi_ | [**getIdentityResourceFileById**](docs/Api/IdentityApi.md#getidentityresourcefilebyid) | **GET** /identity/{id}/resources/{resource_id}/resource_files/{resource_file_id} | Get resource file    |
| _IdentityApi_ | [**listIdentities**](docs/Api/IdentityApi.md#listidentities)                           | **GET** /identities                                                              | List identities      |
| _IdentityApi_ | [**listIdentityResources**](docs/Api/IdentityApi.md#listidentityresources)             | **GET** /identity/{id}/resources                                                 | List resources       |
| _ProjectApi_  | [**getSettings**](docs/Api/ProjectApi.md#getsettings)                                  | **GET** /settings                                                                | Get project settings |

## Documentation For Models

- [Cursor](docs/Model/Cursor.md)
- [Identity](docs/Model/Identity.md)
- [IdentityOwner](docs/Model/IdentityOwner.md)
- [IdentityResource](docs/Model/IdentityResource.md)
- [PaginatedIdentities](docs/Model/PaginatedIdentities.md)
- [PaginatedResources](docs/Model/PaginatedResources.md)
- [ProjectSettings](docs/Model/ProjectSettings.md)
- [ProjectSettingsCustomizations](docs/Model/ProjectSettingsCustomizations.md)
- [ProjectSettingsVerificationSteps](docs/Model/ProjectSettingsVerificationSteps.md)
- [Resource](docs/Model/Resource.md)
- [ResourceFile](docs/Model/ResourceFile.md)
- [ResourceInput](docs/Model/ResourceInput.md)
- [User](docs/Model/User.md)
- [WatchlistResponse](docs/Model/WatchlistResponse.md)

## Documentation For Authorization

## IdentityAccessToken

- **Type**: Bearer authentication (JWT)

## PublishableApiKey

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header

## SecretApiKey

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header

## Author
