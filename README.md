# omc-executable
## How to run
* Keep default settings in application.properties, run:
```
  java -jar omc-test-service-0.0.1-SNAPSHOT.jar
```
* Custom settings in application.properties. Change the settings in application.properties and run:
```
  java -jar -Dspring.config.location=. omc-test-service-0.0.1-SNAPSHOT.jar
```
## Features
* Using Tomcat as http server to receive requests
* Request/Delivery Queue, when request queue is full, reject the request
* Request/Delivery threads number, configurable number of threads for request/delivery worker threads
* Service Register, using zookeeper as Service Registry
* Service Discovery, using zookeeper as Service Discovery
* If specify next Micro Service name, find the service through Service Discovery and send request through http call

## Run with command line arguments
* java -jar omc-test-service-0.0.1-SNAPSHOT.jar --server.port=9000 --zookeeper.host=127.0.0.1 --zookeeper.port=2181 --omc.service.name=OMC_EventMgr_TestService --omc.request.queue.max.size=10 --omc.delivery.queue.max.size=10 --omc.request.task.thread.size=1 --omc.delivery.task.thread.size=1 --omc.service.registry.mode=zookeeper --omc.service.registry.name=/OMC/EventMgr/TestService --omc.delivery.mode=/OMC/EventMgr/TestService --omc.delivery.retry.count=1000 --omc.service.discovery.mode=zookeeper --logging.level.com.omc=DEBUG --logging.file=omc.log
