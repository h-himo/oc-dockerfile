# opensource COBOL for Docker

opensource COBOL and Open COBOL ESQL development environment on AlmaLinux

Versions :
- OS: AlmaLinux 9
- opensource COBOL: 1.5.2J
- Open COBOL ESQL: 1.3

Sample :

To build a sample image.
```
docker build . -t opensourcecobol/opensource-cobol-almalinux9
docker run -itd -v /c/Develop/share:/root/share --name oc152alma opensourcecobol/opensource-cobol-almalinux9
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

Copyright 2024, Tokyo System House Co., Ltd. <opencobol@tsh-world.co.jp>
