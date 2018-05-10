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

## Pricing

### Number of requests

1 million requests are free. $0.20 per 1m requests after

### Duration

- max 5 minutes
- $0.00001667 for every GB-second used

## Lambda triggers

* API gateway
* AWS IoT

## Tips

- 1 event can trigger n functions
- AWS X-ray allows you to debug what is happening
- lambda can do thing globally
- know your triggers