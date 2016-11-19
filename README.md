## Alpine based aws command line client

This container runs the following:

`aws-cli/1.11.19 Python/2.7.12 Linux/4.4.27-moby botocore/1.4.76`

##### Simple usage

1. `docker run -it --rm -v ~/.aws:/root/.aws spantree/awscli s3 ls`
2. `docker run -it --rm -v ~/.aws:/root/.aws spantree/awscli --profile=myprofile s3 ls`
3. `docker run -it --rm -e AWS_PROFILE=myprofile -v ~/.aws:/root/.aws spantree/awscli s3 ls`

##### Advanced usage (login into the the container)

`docker run -it --rm -v ~/.aws:/root/.aws --entrypoint /bin/bash spantree/awscli -l` and then use `aws <command>`


