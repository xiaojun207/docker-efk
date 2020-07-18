# docker-efk
docker-compose efk, (elasticsearch、fluentd、kibana)

## docker-compose
```
  docker-compose -d up
```

## eg.
```
docker stop fluentd-test 
docker rm fluentd-test 
docker run -d --name fluentd-test --log-driver fluentd --log-opt fluentd-address=localhost:24224 --log-opt tag="log-test-container-A" busybox sh -c 'for((i=1;i<=10;i++));do echo "${date} this is ${i} log message"; sleep 1; done;'
```

## 其中镜像：xiaojun207/fluentd-es:v1.11.3
```
    https://github.com/xiaojun207/fluentd-es.git
```
>fluentd-es:v1.11.3版本，新版本fluentd内置配置文件，支持java多行日志文件。  
>elasticsearch地址可以通过: --add-host elasticsearch:192.168.1.33
>
