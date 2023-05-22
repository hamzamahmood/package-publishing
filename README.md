
# Getting Started with APIMATIC Calculator

## Introduction

Simple calculator API hosted on APIMATIC

## Install the Package

Install the gem from the command line:

```ruby
gem install apimatic-calculator-test-api-sdk -v 2.4.5
```

Or add the gem to your Gemfile and run `bundle`:

```ruby
gem 'apimatic-calculator-test-api-sdk', '2.4.5'
```

For additional gem details, see the [RubyGems page for the apimatic-calculator-test-api-sdk gem](https://rubygems.org/gems/apimatic-calculator-test-api-sdk/versions/2.4.5).

## Test the SDK

To run the tests, navigate to the root directory of the SDK in your terminal and execute the following command:

```
rake
```

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/hamzamahmood/package-publishing/tree/2.4.5/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| `environment` | Environment | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| `connection` | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| `adapter` | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| `timeout` | `Float` | The value to use for connection timeout. <br> **Default: 60** |
| `max_retries` | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| `retry_interval` | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| `backoff_factor` | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| `retry_statuses` | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| `retry_methods` | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| `http_callback` | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |

The API client can be initialized as follows:

```ruby
client = ApimaticCalculator::Client.new(
  environment: Environment::PRODUCTION
)
```

## List of APIs

* [Simple Calculator](https://www.github.com/hamzamahmood/package-publishing/tree/2.4.5/doc/controllers/simple-calculator.md)

## Classes Documentation

* [Utility Classes](https://www.github.com/hamzamahmood/package-publishing/tree/2.4.5/doc/utility-classes.md)
* [HttpResponse](https://www.github.com/hamzamahmood/package-publishing/tree/2.4.5/doc/http-response.md)
* [HttpRequest](https://www.github.com/hamzamahmood/package-publishing/tree/2.4.5/doc/http-request.md)

