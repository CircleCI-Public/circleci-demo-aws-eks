# CircleCI Demo: AWS EKS [![CircleCI status](https://circleci.com/gh/CircleCI-Public/circleci-demo-aws-eks.svg "CircleCI status")](https://circleci.com/gh/CircleCI-Public/circleci-demo-aws-eks)

## Deploy to AWS Elastic Container Service for Kubernetes (AWS EKS) via CircleCI 2.0 using Orbs (Example Project)
This project provides an example of how to use orbs to conveniently build a Docker image on [CircleCI](https://circleci.com), push the Docker image to an Amazon Elastic Container Registry (ECR), and then deploy to Amazon Elastic Container Service for Kubernetes (AWS EKS). In particular, the [aws-ecr](https://circleci.com/orbs/registry/orb/circleci/aws-ecr) and the [aws-eks](https://circleci.com/orbs/registry/orb/circleci/aws-eks) Orbs will be used in this project.

### Configure environment variables on CircleCI
The following [environment variables](https://circleci.com/docs/2.0/env-vars/#setting-an-environment-variable-in-a-project) must be set for the project on CircleCI via the project settings page, before the project can be built successfully.


| Variable                       | Description                                               |
| ------------------------------ | --------------------------------------------------------- |
| `AWS_ACCESS_KEY_ID`            | Used by the AWS CLI |
| `AWS_SECRET_ACCESS_KEY `       | Used by the AWS CLI |
| `AWS_DEFAULT_REGION`           | Used by the AWS CLI. Example value: "eu-west-3" (The specified region should be supported by AWS EKS) |
| `AWS_ECR_URL`                  | Identifies the AWS ECR docker image registry that the docker image will be pushed to, in the format `AWS_ACCOUNT_ID`.dkr.ecr.`AWS_DEFAULT_REGION`.amazonaws.com |

## Useful Links & References
- https://circleci.com/orbs/registry/orb/circleci/aws-ecr
- https://circleci.com/orbs/registry/orb/circleci/aws-eks
- https://github.com/CircleCI-Public/aws-ecr-orb
- https://github.com/CircleCI-Public/aws-eks-orb