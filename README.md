# docker-fluentd-multiprocess

```console
$ docker-compose up --force-recreate --build -d
$ parallel curl -s 127.0.0.1 > /dev/null ::: `seq 1 10`
```

```console
$ docker-compose logs fluentd-out
...
fluentd-out_1      | 2017-05-30 15:05:17 +0000 child1.docker.dockerfluentdmultiprocess_nginx_1: {"method":"GET","path":"/","code":"200"}
fluentd-out_1      | 2017-05-30 15:05:17 +0000 child1.docker.dockerfluentdmultiprocess_nginx_1: {"method":"GET","path":"/","code":"200"}
fluentd-out_1      | 2017-05-30 15:05:17 +0000 child1.docker.dockerfluentdmultiprocess_nginx_1: {"method":"GET","path":"/","code":"200"}
...
```
