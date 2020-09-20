# Docker Images

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<details>
<summary>Details</summary>

- [Login](#login)
- [GRAPE](#grape)
- [AutoML-Zero](#automl-zero)
  - [Setup dataset](#setup-dataset)

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

## AutoML-Zero
### Setup dataset
```shell script
docker pull docker.pkg.github.com/automatic-programming/docker-images/dataset:v0.1.1

mkdir -p test_data
docker run -v `pwd`/test_data:/test_data -it --rm dataset:v0.1.1
```

```shell script
docker pull docker.pkg.github.com/automatic-programming/docker-images/automl-zero:v0.1.1

rm -rdf output
mkdir output
docker run -v `pwd`/test_data:/test_data -v `pwd`/output:/output -it --rm docker.pkg.github.com/automatic-programming/docker-images/automl-zero:v0.1.1
```
