# JFaiss-CPU **(Linux only)**

Faiss (CPU) bindings for Java 
Supports version 1.6.3 of Faiss, compiled with optimized flags for centOS.

## Adding JFaiss-CPU to you build

To add a dependency on JFaiss-CPU using Maven, use

```xml
<dependency>
  <groupId>com.github.victor-paltz</groupId>
  <artifactId>JFaiss-CPU</artifactId>
  <version>1.3.4</version>
</dependency>
```


## Requirement

- JDK v1.8
- Apache Maven v3.6.3
- Docker v19.03.12

## Build JAR (maven)

Run the test cases
```sh
mvn clean test -Dtest=FaissTestRunner
```

Creating a JAR
```sh
mvn package
```

## Building from source (docker)

Install faiss and generate required Java files
```sh
git clone https://github.com/victor-paltz/JFaiss-CPU.git
cd JFaiss-CPU
git submodule update --init
docker build -t jfaiss-source .
```
This will generate required `.java` files from `swigfaiss.swig`

## To-do

* [x] Publish to mvn
* [ ] GPU support

## Reference

- <https://github.com/gameofdimension/jni-faiss>
- <https://github.com/adamheinrich/native-utils>
- <https://github.com/thenetcircle/faiss4j>
