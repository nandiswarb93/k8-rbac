
eksctl utils associate-iam-oidc-provider --cluster roboshop-dev --approve

eksctl create iamserviceaccount --cluster <cluster-name> --name <service-account-name> --namespace <namespace> --attach-policy-arn <IAM-policy-ARN> --approve

eksctl create iamserviceaccount --cluster roboshop-dev --name secret-reader --namespace roboshop --attach-policy-arn arn:aws:iam::200651372723:policy/RoboShopMySQLSecretReader --approve
