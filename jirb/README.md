# JIRB Docker image

## What are the differences between this image and [library/java](https://github.com/dockerfile/java)?

* Uses [dockerfile/debian:jessie](https://registry.hub.docker.com/_/debian/) instead of [Ubuntu](https://github.com/dockerfile/ubuntu).
* Uses [Oracle Server JRE](http://www.oracle.com/technetwork/java/javase/downloads/server-jre8-downloads-2133154.html) instead of [OpenJDK](http://openjdk.java.net/).
* Installs [Java Cryptography Extension (JCE)](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html).
* Installs [Bouncy Castle JCE](http://www.bouncycastle.org/java.html) JCE provider.
* Adds [JRuby](http://jruby.org/) interactive interpreter.

## Examples

### Default jirb/irb as PID1

Simply launch Docker container:

    [root@docker-host ~]# docker run -it bartprokop/jirb
    irb(main):001:0>

### Starting jirb/irb from command line

If you run bash, as your PID1 process, irb is accessible from command line.

    [root@docker-host ~]# docker run -it bartprokop/jirb /bin/bash
    root@f93e2a192f93:/# irb
    irb(main):001:0> exit
    
    root@f93e2a192f93:/# jirb
    irb(main):001:0> exit

### Java command line

Java is available via command line, i.e. to run Spring-Boot microservices.

    [root@docker-host ~]# docker run -it bartprokop/jirb /bin/bash
    root@f93e2a192f93:/# java -version
    java version "1.8.0_92"
    Java(TM) SE Runtime Environment (build 1.8.0_92-b14)
    Java HotSpot(TM) 64-Bit Server VM (build 25.92-b14, mixed mode)
    root@f93e2a192f93:/#

Note that you shall not use this Docker image as Oracle Java redistributable
image, as such use might be violation of Java licence. This Docker image provides
third party software - here irb that runs on top of JVM. Despite it is technically
feasible to use this as microservice base Java image, such use is discouraged due
to licencing concerns.

If you like this image and its production readiness, please use GitHub avaiable
resources to build your own base image and distribute it via your internal registry.

### That's all folks.
