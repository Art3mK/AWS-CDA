# Lambda

Lamba scales out automatically

* event-driven compute service
* compute service: HTTP request -> API gateway -> Lambda function (separate instance for each request)

## Languages

* nodejs
* java
* python
* C#
* Go

## event sources

- S3
- DynamoDB
- Kinesis (Data streams, Data firehose)
- SNS
- SES
- Cognito
- Cloudformation
- Clouwatch logs/events
- codecommit
- Config
- Alexa
- Lex
- API gateway
- IoT Button
- CloudFront
- custom events

## Pricing

### Number of requests

1 million requests are free. $0.20 per 1m requests after

### Duration

- default timeout is 3 seconds
- max 5 minutes
- $0.00001667 for every GB-second used

## Resources

You cant set your memory in 64Mb increments from 128Mb to 3Gb.

Each Lambda function receives 500MB of non-persistent disk space in its own /tmp directory.

for outbound connections only TCP/IP sockets are supported, and ptrace (debugging) system calls are blocked. TCP port 25 traffic is also blocked

## Lambda triggers

* API gateway
* AWS IoT

## Tips

- 1 event can trigger n functions
- AWS X-ray allows you to debug what is happening
- lambda can do thing globally
- know your triggers
