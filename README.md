# Docker Images

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<details>
<summary>Details</summary>

- [Login](#login)
- [GRAPE](#grape)

</details>
<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Login
```shell script
echo <TOKEN> | docker login docker.pkg.github.com -u <USERNAME> --password-stdin
```

## GRAPE
```shell script
docker pull docker.pkg.github.com/automatic-programming/docker-images/grape:v0.0.4

rm -rdf output
mkdir output
docker run -v `pwd`/output:/output -it --rm docker.pkg.github.com/automatic-programming/docker-images/grape:v0.0.4
```
