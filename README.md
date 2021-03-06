# ebay_sell_metadata_v1_oas2_php
The Metadata API has operations that retrieve configuration details pertaining to the different eBay marketplaces. In addition to marketplace information, the API also has operations that get information that helps sellers list items on eBay.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1.3.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/nopolabs/ebay_sell_metadata_v1_oas2_php.git"
    }
  ],
  "require": {
    "nopolabs/ebay_sell_metadata_v1_oas2_php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/ebay_sell_metadata_v1_oas2_php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: Client Credentials
$config = Nopolabs\EBay\Sell\Metadata\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Nopolabs\EBay\Sell\Metadata\Api\CountryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = "country_code_example"; // string | This path parameter specifies the two-letter ISO 3166-1 Alpha-2 country code for the country whose jurisdictions you want to retrieve. eBay provides sales tax jurisdiction information for Canada, India, and the United States.Valid values for this path parameter are CA, IN, and US.

try {
    $result = $apiInstance->getSalesTaxJurisdictions($country_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CountryApi->getSalesTaxJurisdictions: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.ebay.com/sell/metadata/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CountryApi* | [**getSalesTaxJurisdictions**](docs/Api/CountryApi.md#getsalestaxjurisdictions) | **GET** /country/{countryCode}/sales_tax_jurisdiction | 
*MarketplaceApi* | [**getAutomotivePartsCompatibilityPolicies**](docs/Api/MarketplaceApi.md#getautomotivepartscompatibilitypolicies) | **GET** /marketplace/{marketplace_id}/get_automotive_parts_compatibility_policies | 
*MarketplaceApi* | [**getItemConditionPolicies**](docs/Api/MarketplaceApi.md#getitemconditionpolicies) | **GET** /marketplace/{marketplace_id}/get_item_condition_policies | 
*MarketplaceApi* | [**getListingStructurePolicies**](docs/Api/MarketplaceApi.md#getlistingstructurepolicies) | **GET** /marketplace/{marketplace_id}/get_listing_structure_policies | 
*MarketplaceApi* | [**getNegotiatedPricePolicies**](docs/Api/MarketplaceApi.md#getnegotiatedpricepolicies) | **GET** /marketplace/{marketplace_id}/get_negotiated_price_policies | 
*MarketplaceApi* | [**getProductAdoptionPolicies**](docs/Api/MarketplaceApi.md#getproductadoptionpolicies) | **GET** /marketplace/{marketplace_id}/get_product_adoption_policies | 
*MarketplaceApi* | [**getReturnPolicies**](docs/Api/MarketplaceApi.md#getreturnpolicies) | **GET** /marketplace/{marketplace_id}/get_return_policies | 


## Documentation For Models

 - [AutomotivePartsCompatibilityPolicy](docs/Model/AutomotivePartsCompatibilityPolicy.md)
 - [AutomotivePartsCompatibilityPolicyResponse](docs/Model/AutomotivePartsCompatibilityPolicyResponse.md)
 - [Error](docs/Model/Error.md)
 - [ErrorParameter](docs/Model/ErrorParameter.md)
 - [Exclusion](docs/Model/Exclusion.md)
 - [ItemCondition](docs/Model/ItemCondition.md)
 - [ItemConditionPolicy](docs/Model/ItemConditionPolicy.md)
 - [ItemConditionPolicyResponse](docs/Model/ItemConditionPolicyResponse.md)
 - [ListingStructurePolicy](docs/Model/ListingStructurePolicy.md)
 - [ListingStructurePolicyResponse](docs/Model/ListingStructurePolicyResponse.md)
 - [NegotiatedPricePolicy](docs/Model/NegotiatedPricePolicy.md)
 - [NegotiatedPricePolicyResponse](docs/Model/NegotiatedPricePolicyResponse.md)
 - [ProductAdoptionPolicy](docs/Model/ProductAdoptionPolicy.md)
 - [ProductAdoptionPolicyResponse](docs/Model/ProductAdoptionPolicyResponse.md)
 - [ReturnPolicy](docs/Model/ReturnPolicy.md)
 - [ReturnPolicyDetails](docs/Model/ReturnPolicyDetails.md)
 - [ReturnPolicyResponse](docs/Model/ReturnPolicyResponse.md)
 - [SalesTaxJurisdiction](docs/Model/SalesTaxJurisdiction.md)
 - [SalesTaxJurisdictions](docs/Model/SalesTaxJurisdictions.md)
 - [TimeDuration](docs/Model/TimeDuration.md)


## Documentation For Authorization


## Client Credentials

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
 - **https://api.ebay.com/oauth/api_scope**: View public data from eBay


## Author




