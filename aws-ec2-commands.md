# Get key-pair 
```
aws ec2 describe-key-pairs|awk '/KeyName/{print $2}'
```

# SecurityGroups
## Get security Groups
```
aws ec2 describe-security-groups | awk '/GroupName/{print $2}'
```
## Delete security groups
```
aws ec2 delete-security-group --group-name AWS-OpsWorks-Java-App-Server
```
### Create Security Groups
```
aws ec2 create-security-group --description 'cli created group' --group-name cli-sg
```
### Add rules in security group
```
aws ec2 authorize-security-group-ingress --group-name cli-sg --protocol tcp --port 22 --cidr 0.0.0.0/0
```


# Create EC2 Instance
```
aws ec2 run-instances --image-id ami-041d6256ed0f2061c --instance-type t2.micro --key-name aws-devops-kp --security-group-ids sg-07649d370f7e0a6e7 
```
