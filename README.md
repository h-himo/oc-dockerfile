# opensource COBOL for Docker

opensource COBOL and Open COBOL ESQL development environment

Versions :
- CentOS: AlmaLinux 9
- opensource COBOL: 1.5.2J
- Open COBOL ESQL: 1.3

Sample :

To build a sample image.
```
docker build . -t opensourcecobol/opensource-cobol-almalinux9
wget -O src/HELLO.cbl https://raw.githubusercontent.com/opensourcecobol/oc-dockerfile/master/HELLO.cbl
docker run --rm -it -v `pwd`/src:/oscobol/src:ro --name oscobol opensourcecobol/opensource-cobol-almalinux9
```

in docker container

```
cobc src/HELLO.cbl
cobcrun HELLO
```

display your console `HELLO WORLD!`

When you want stop container, follow command:

```
docker stop oscobol
```

Copyright 2023, Tokyo System House Co., Ltd. <opencobol@tsh-world.co.jp>
