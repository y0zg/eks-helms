

**External-dns helm chart**

Usage:

helm install external-dns . --set externDns.domainName=scoring.com --set serviceAccount=external-dns-k8s

**IAM Service Account** 

external-dns-k8s policies reqired.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "route53:ChangeResourceRecordSets"
            ],
            "Resource": "arn:aws:route53:::hostedzone/*",
            "Effect": "Allow"
        }
    ]
}
```

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "route53:ListHostedZones",
                "route53:ListResourceRecordSets",
                "route53:ListTagsForResource"
            ],
            "Resource": "*",
            "Effect": "Allow"
        }
    ]
}
```