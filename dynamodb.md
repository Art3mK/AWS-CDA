# DynamoDB

FAQ - √
Amazon DynamoDB stores three geographically distributed replicas of each table to enable high availability and data durability

- supports atomic updates
- runs exclusively on SSDs

## consistency models

### Eventually consistent reads (default)

- maximize read throughput
- might not reflect the results of a recently completed write
- consistency across all copies of data is usually reached within a second

### Strongly consistent reads

- returns a result that reflects all writes that received a successful response prior to the read

## queries

- GET/PUT using a user-defined primary key

