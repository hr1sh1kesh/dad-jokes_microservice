# Dad Jokes Microservice #
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/0ckh82ned3gipoy2o03m.jpg)

[![GitHub release](https://img.shields.io/github/release/yesinteractive/dad-jokes_microservice.svg)](https://github.com/yesinteractive/dad-jokes_microservice) 
![Packagist](https://img.shields.io/packagist/l/fsl/fsl.svg) ![PHP from Packagist](https://img.shields.io/packagist/php-v/fsl/fsl.svg)

Just a sample microservice used for testing Kong API Gateway, Kubernetes K8s, Docker, Kuma Service mesh, Istio Service Mesh, etc. Feel free to add your own jokes to this repo as well.

## Usage ##

**Response Code** : `200 OK`

```json
{
  "Jokes": {
    "Opener": "What did the mountain climber name his son?",
    "Punchline": "Cliff"
  }
}
```

### Deployment Examples ###

See usage examples for Kubernetes, Kong for Kubernetes Ingress Controller, and docker-compose in the [examples directory folder.](https://github.com/yesinteractive/dad-jokes_microservice/blob/master/examples)

### With Docker ###

Docker image is Alpine 3.11 based running PHP 7.3 on Apache. The containter exposes both ports 80 an 443 with a self signed certificated. If you wish to alter the container configuration, feel free to use the Dockerfile in this repo (https://github.com/yesinteractive/dad-jokes_microservice/blob/master/Dockerfile). Otherwise, you can pull the latest image from DockerHub with the following command:
```
docker pull yesinteractive/dadjokes
```
Typical basic usage:

```
docker run -it yesinteractive/dadjokes
```

Typical usage in Dockerfile:

```
FROM yesinteractive/dadjokes
RUN echo <your commands here>
```


