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
