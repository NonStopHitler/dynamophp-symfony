DynamoPHP Symfony Bundle
================
![License](https://img.shields.io/github/license/edumarques/dynamophp)
![Build Status](https://github.com/edumarques/dynamophp/actions/workflows/base.yml/badge.svg)

---

The **DynamoPHP Symfony Bundle** integrates [DynamoPHP](https://github.com/edumarques/dynamophp)
into [Symfony](https://symfony.com) applications, providing seamless configuration and service registration for Amazon
DynamoDB operations.

## Features

- Auto-wiring of DynamoPHP services
- Configurable AWS SDK DynamoDB client and Marshaler
- Symfony Flex recipe support for automatic configuration
- Sandbox application for testing and development

## Installation

Install via Composer:

```shell
composer require edumarques/dynamophp-symfony
```

Ensure that your Symfony application is configured to use Symfony Flex for automatic bundle registration and
configuration.

## Configuration

**Note: this is an optional step. By default, the bundle assumes _DynamoDBClient_ and _Marshaler_ services are already
registered in the application DI container.**

After installation, you can configure the bundle by creating a `dynamo_php.yaml` file in your `config/packages/`
directory:

```yaml
# config/packages/dynamo_php.yaml
dynamo_php:
  client:
    region: 'us-east-1'
    version: 'latest'
    # Add DynamoDB client configuration options here
  marshaler:
  # Add Marshaler configuration options here
```

Adjust the client and marshaler settings according to your AWS DynamoDB setup and application requirements.

## Usage

Once configured, you can inject DynamoPHP services into your Symfony services or controllers. For example, to use the
EntityManager:

```php
use EduardoMarques\DynamoPHP\ODM\EntityManager;

class YourService
{
    public function __construct(
        private EntityManager $entityManager,
    ) {
    }

    // Your methods here
}
```

## Contributing

Contributors are always welcome! For more information on how you can contribute, please read
our [contribution guideline](CONTRIBUTING.md).

For any questions, feel free to reach out to me directly by
email: [eduardomarqs1@gmail.com](mailto:eduardomarqs1@gmail.com).

For more information on DynamoPHP, visit the [DynamoPHP repository](https://github.com/edumarques/dynamophp).
