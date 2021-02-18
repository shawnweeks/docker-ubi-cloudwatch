### Download Dependencies
```shell
wget https://s3.amazonaws.com/amazoncloudwatch-agent/redhat/amd64/latest/amazon-cloudwatch-agent.rpm
```

### Build Image
```shell
docker build \
    -t ${REGISTRY}/aws/cloudwatch-agent \
    --build-arg BASE_REGISTRY=${REGISTRY} .
```

### Push to Docker Registry
```shell
docker push ${REGISTRY}/aws/cloudwatch-agent
```