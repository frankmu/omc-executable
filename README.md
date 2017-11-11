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
