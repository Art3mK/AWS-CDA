# Simple Workflow Service

- coordination of tasks
- tasks represent invocations of various prosessing steps (code|web calls|human actions|scripts)
- workers are programs that interact with SWF
- decider controls the coordination of tasks
- SWF stores tasks, monitors progress and ensures that a task is assigned only once and is never duplicated
- SWF maintains app's state durably, workers and deciders don't have to keep track of execution state
- SFW domains isolate a set of types, executions, and task lists from others within the same account
- https:/swf.us-east-1.amazonaws.com `RegisterDomain`
- max workflow can be `1 year` and the value is always measured in seconds
- SWF presents task-oriented API (with SQS - message oriented API)