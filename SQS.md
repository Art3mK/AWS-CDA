# SQS

distributed queue system

- messages can contain up to 256Kb of text in any format.
- ensures delivery of each message at least once
- no first in, first out delivery of messages, message can be delivered multiple times in any order
- 30 seconds default timeout, 12 hours visilibity timeout max, `ChangeMessageVisilility` restarts timeout period using new value.
- billed at 64Kb "chunks"
- first 1M sqs requests are free
- single request can have from 1 ti 10 messages
- each 64Kb is billed as 1 request
- 0.5$ per 1M requests per month
- SQS long polling, doesn't return a response until a message arrives, or the long poll times out (max long poll timeout = 20 seconds)
- max retention period for message: 14 days

Visibility timeout starts when worker pulls message from the queue. If processing successfull -> remove message from queue. If no - after visilibily timeout message will appear in queue again.

## Fan out

Message -> SNS topic -> multiple SQL queues.