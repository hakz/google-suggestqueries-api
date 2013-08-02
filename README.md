# Google SuggestQueries API Client

## Installation

Install via composer:

```yaml
{
    "require": {
        "wildlyinaccurate/google-suggestqueries-api" : "1.0.*"
    }
}
```
> `google-suggestqueries-api` follows the PSR-0 convention names for its classes, which means you can easily integrate `google-suggestqueries-api` classes loading in your own autoloader.

## Basic usage

```php
<?php

// This file is generated by Composer
require_once 'vendor/autoload.php';

$client = new Google\SuggestQueries\Client;

// $client->getClient() is an instance of Buzz\Client\Curl, so you can set
// various options before performing a query:
$client->getClient()->setProxy('proxyhost:8080');

$suggestions = $client->getSuggestions($query);

// Suggestions can be sorted by their num_queries value:
$sortedSuggestions = $suggestions->sortByNumQueries();
```

## Contributing

When submitting pull requests, please include any relevant tests and ensure the entire test suite passes: `$ phpunit --bootstrap tests/bootstrap.php tests`
