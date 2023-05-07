# AWS Lambda Function to Delete Old OpenSearch Indices

A Python-based AWS Lambda function that deletes old indices in OpenSearch based on a user-specified age.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- Deletes OpenSearch indices older than a user-specified age
- Configurable OpenSearch endpoint and index name
- Handles retry attempts for OpenSearch operations

## Requirements

- An AWS account with access to Lambda and OpenSearch services
- Python 3.x


## Configuration

To use this code, you need to update the JSON event passed to the Lambda function:

1. Set the `es_endpoint` field to your OpenSearch endpoint.
2. Set the `delete_after` field to the number of days after which indices should be deleted.
3. Set the `index` field to the base name of the indices you want to delete, without the date.
4. Set the `es_max_retry` field to the maximum number of retries for OpenSearch operations.

## Deployment

Follow these steps to deploy the Lambda function:

1. Create a Lambda function in the AWS Management Console or using the AWS CLI.
2. Upload the source code, either by zipping the files and uploading through the console, or using the AWS CLI.
3. Set the Lambda function handler, runtime, and other configurations as needed.
4. Add necessary triggers, such as CloudWatch events or other AWS services, to invoke the Lambda function.
5. Test the Lambda function by passing the JSON event with the appropriate configuration.

## Contributing

Contributions are welcome. To contribute, please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request
