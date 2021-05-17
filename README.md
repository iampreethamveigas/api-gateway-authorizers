# jwtAuthorizer - Custom JWT AWS Lambda Authorizer for Amazon API Gateway

 `Bearer` format from `Authorization` HTTP header.


Secret and claims can be different for every used stage environment.
In this example, **jwtAuthorizr** lambda function reads them from environment variables which should be baked into the function deployment for each stage.
But Lambda could also load them from e.g. S3 or DynamoDB or something completely different.

The token in the test event in `test.json` uses these secrets and claims:
- `iss`: dasniko
- `aud`: demo
- `secret`: secret
