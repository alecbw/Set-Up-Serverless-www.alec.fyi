# Set-Up-Serverless-www.alec.fyi

# Related article

https://www.alec.fyi/set-up-serverless.html

# Using this

This repo contains a serverless.yml infrastructure-as-code file, which deploys 1 Lambdas

* `test-lambda`

Deploys are managed through a CloudFormation Stack (called `test-stack`)

To create the CloudFormation Stack (and also subsequently update it), use:
``` 
sls deploy
```

You can test the Lambda locally
```
sls invoke local -f test-lambda -d {"key1": "value1", "key2":2}
```

All the resources fit easily in the AWS Free Tier and should have no ongoing costs

To take down the CloudFormation Stack and associated Lambdas and S3, use:
```
sls remove
```
