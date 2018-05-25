# Cloudwatch

FAQ - √

- CloudWatch does not support metric deletion.
- CloudWatch stores metrics for terminated Amazon EC2 instances or deleted Elastic Load Balancers for 15 months.
- Alarm history is available for 14 days
---

performance monitoring

- Standard = 5 minutes
- Detailed = 1 minute

---

* Dashboards
* Alarms
* Events
* Logs
    - real time application and system monitoring
        ```
        CloudWatch Logs can track the number of errors that occur in your application logs and send you a notification whenever the rate of errors exceeds a threshold you specify.
        ```
    - long term log retention
        ```
        You can use CloudWatch Logs to store your log data indefinitely in highly durable and cost effective storage without worrying about hard drives running out of space. The CloudWatch Logs Agent makes it easy to quickly move both rotated and non rotated log files off of a host and into the log service. You can then access the raw log event data when you need it.
        ```
    - Cloudwatch agent log
        * Supported platforms:
            - Amazon Linux
            - Ubuntu
            - CentOS
            - Red Hat Enterprise Linux
            - Windows

## Retention period

* Data points with a period of less than 60 seconds are available for 3 hours. These data points are high-resolution custom metrics.
* Data points with a period of 60 seconds (1 minute) are available for 15 days
* Data points with a period of 300 seconds (5 minute) are available for 63 days
* Data points with a period of 3600 seconds (1 hour) are available for 455 days (15 months)