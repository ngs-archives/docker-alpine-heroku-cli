docker-alpine-heroku-cli
========================

[![Docker Automated build](https://img.shields.io/docker/automated/atsnngs/alpine-heroku-cli.svg?maxAge=2592000)](https://hub.docker.com/r/atsnngs/alpine-heroku-cli/)

Usage
-----

### CircleCI

```yaml
# .circleci/config.yml
version: 2

jobs:
  deploy:
    docker:
      - image: atsnngs/alpine-heroku-cli:latest
    steps:
      - checkout
      - add_ssh_keys:
          fingerprints:
            - '4d:74:c3:f5:28:7d:ed:db:aa:b8:6c:7d:15:98:8a:5b'
      - run: /bin/sh /setup.sh
      - run: git push heroku master
```
