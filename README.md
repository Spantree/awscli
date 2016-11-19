## Alpine based aws command line client


##### Simple usage

1. `docker run -it --rm -v ~/.aws:/root/.aws spantree/awscli s3 ls`
2. `docker run -it --rm -v ~/.aws:/root/.aws spantree/awscli --profile=myprofile s3 ls`
3. `docker run -it --rm -e AWS_PROFILE=myprofile -v ~/.aws:/root/.aws spantree/awscli s3 ls`

##### Advanced usage (login into the the container)

`docker run -it --rm -v ~/.aws:/root/.aws --entrypoint /bin/bash spantree/awscli -l` and then use `aws <command>`


