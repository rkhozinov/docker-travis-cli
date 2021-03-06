# docker-travis-cli

Travis CLI in a `ruby:alpine` image.

## Pull and tag
```shell
docker pull caktux/travis-cli
docker tag caktux/travis-cli travis-cli
```

## Encrypting environment variables
```shell
docker run --rm travis-cli encrypt SECRET=123 -r org/repo
```

## Interactive setup of `.travis.yml`
```
docker run --rm -it -v ~/project:/project travis-cli setup pypi
```

## Validating your `.travis.yml` with travis-lint
```shell
docker run --rm -v ~/project:/project --entrypoint=travis-lint travis-cli /project/.travis.yml
```
