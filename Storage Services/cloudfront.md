# Cloudfront

## Edge location

- Location where content will be cached
- not just READ only, you can write to them too.
- object are cached for the life of the TTL
- clean cached objects - $$

## Origin

Origin of all the files that the CDN will distribute. Could be multiple per distribution.

- S3
- EC2 instances
- ELB
- Route53
- non-AWS origin server

## Distribution

Name given the CDN, which consists of a collection of edge locations

### Access restrictions

- Black/White listing available

### Web distribution

### RTMP distribution