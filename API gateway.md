# API gateway


- https only, can provide own certificate
- stages from dev, production, etc, similar to tags. They define the path through which the deployment is accessible.
- stage can contain variables
- multiple versions of the same REST API
- no VPC endpoint, but support VPC links
- support auth for API methods (AWS signature version 4, lambda authorizers)
- gateway can generate API keys and associate them with an usage plan. Call are monitored and included in cloudwatch
- throttling/standard rate limit/burst rate limit per second
- automatic DDoS protection
- gateway can generate client-side SSL certificates to authenticate to backend.
### API caching

caching for a stage, gateway caches responses from your endpoint fro a specified TTL in seconds

bills as normal calls

### Backends

- lambda
- AWS step functions
- call HTTP endpoint hosted on Beanstalk, EC2, non-AWS hosted
- static content (mocks)
- Kinesis, some other AWS services