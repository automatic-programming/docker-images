# Docker Images

## Login
```shell script
echo <TOKEN> | docker login docker.pkg.github.com -u <USERNAME> --password-stdin
```

## GRAPE
```shell script
docker pull docker.pkg.github.com/automatic-programming/docker-images/grape:v0.0.3

rm -rdf output
mkdir output
docker run -v `pwd`/output:/output -it --rm docker.pkg.github.com/automatic-programming/docker-images/grape:v0.0.3
```
