# Create Policy
```
aws iam create-policy --policy-name santapan-s3-custom-policy --policy-document file://s3-custom-policy.json
```
# Create Role

```
aws iam create-role --role-name santapan-s3-custom-role --assume-role-policy-document file://assume-role-policy-document.json
```

# Attach policy to Roles

```
aws iam attach-role-policy --policy-arn arn:aws:iam::350102312519:policy/santapan-s3-custom-policy --role-name santapan-s3-custom-role
```
# Get role details

```
aws iam get-role --role-name ec2-eks
```



