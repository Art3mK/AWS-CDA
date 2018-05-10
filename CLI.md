## running instances

* describe-instances
* describe-images
* run-instances (to launch new)
* start-instances (to start stopped)
* terminate-instances

```bash
# run-instances
aws ec2 run-instances --security-group-ids sg-ca7b91a0 --subnet-id subnet-6e8d8e16 --key-name 'artem.kajalainen@gofore.com' --count 1 --image-id ami-b144195a --instance-type t2.micro
```