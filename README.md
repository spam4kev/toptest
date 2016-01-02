-  this project plays with deployable container images
-  create a Dockerfile in this github repo with the contents below
```bash
FROM centos
ENTRYPOINT top
```
-  build the container and manually run an instance based on it. then clean up.
```bash
docker build -t toptest .
docker run --name runtoptest -i -t toptest
CTRL+P CTRL+Q
docker rm runtoptest
docker rmi toptest
```

-  OR, a more advanced example, write a docker-compose.yml that deploys it
```bash
runtoptest:
  build: .
  environment:
    TEST: foo
```

  -  Then run it
```bash
docker-compose up
```
