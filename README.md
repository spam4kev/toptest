-  this project plays with deployable container images
-  create a Docker file with contents below
```bash
FROM centos
ENTRYPOINT top
```
-  build the container and run an instance based on it. then clean up.
```bash
docker build --name toptest .
docker run --name runtoptest -i -t toptest
docker rm runtoptest
docker rmi toptest
```
