This a fork using Guzzle 7.

# Chargebee PHP Client Library - API V2

[![Packagist](https://img.shields.io/packagist/v/chargebee/chargebee-php.svg?maxAge=2592000)](https://packagist.org/packages/chargebee/chargebee-php)
[![Packagist](https://img.shields.io/packagist/dt/chargebee/chargebee-php.svg?maxAge=2592000)](https://packagist.org/packages/chargebee/chargebee-php/stats)
[![Packagist](https://img.shields.io/packagist/dm/chargebee/chargebee-php.svg?maxAge=2592000)](https://packagist.org/packages/chargebee/chargebee-php/stats)
[![Packagist](https://img.shields.io/packagist/l/chargebee/chargebee-php.svg?maxAge=2592000)](https://packagist.org/packages/chargebee/chargebee-php)

This is the PHP Library for integrating with Chargebee. Sign up for a Chargebee account [here](https://www.chargebee.com).

Chargebee now supports two API versions - [V1](https://apidocs.chargebee.com/docs/api/v1) and [V2](https://apidocs.chargebee.com/docs/api), of which V2 is the latest release and all future developments will happen in V2. This library is for <b>API version V2</b>. If you’re looking for V1, head to [chargebee-v1 branch](https://github.com/chargebee/chargebee-php/tree/chargebee-v1).

## Requirements

PHP 5.6.0 or later

## Installation

### Composer
```Chargebee``` is available on [Packagist](https://packagist.org/packages/chargebee/chargebee-php) and can be installed using [Composer](https://getcomposer.org/)

<pre><code>composer require deegitalbe/chargebee-php</code></pre>

To use the bindings, 
<pre><code>require_once('vendor/autoload.php');</code></pre>

### Manual Installation
Download the [latest release](https://github.com/chargebee/chargebee-php/releases) and to use the bindings, include 
<code>init.php</code> file. 
<pre><code>require_once('/path/to/chargebee-php/lib/init.php');</code></pre>

## Documentation

* <a href="https://apidocs.chargebee.com/docs/api?lang=php" target="_blank">API Reference</a>

## Usage

To create a new subscription:

<pre><code>
use ChargeBee\ChargeBee\Environment;
use ChargeBee\ChargeBee\Subscription;

...

Environment::configure("your_site", "{your_site_api_key}");
$result = Subscription::create(array(
  "id" => "__dev__KyVqH3NW3f42fD",
  "planId" => "starter",
  "customer" => array(
    "email" => "john@user.com",
    "firstName" => "John",
    "lastName" => "Wayne"
  )
));
$subscription = $result->subscription();
$customer = $result->customer();
$card = $result->card();
</code></pre>

## Legacy Support

If you are using PHP < 5.6.0 , you can download chargebee-php [v2.8.3](https://github.com/chargebee/chargebee-php/tree/v2.8.3). This version will not support recently added features since the version was released. We recommend you to upgrade PHP inorder to use the latest features. 
## License

See the LICENSE file.

