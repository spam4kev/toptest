```bash
docker build --name toptest .
docker run --name runtoptest -i -t toptest
docker rm runtoptest
docker rmi toptest
```
