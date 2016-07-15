# JIRB Docker image

## Examples

### Java command line

Java is available via command line, i.e. to run Spring-Boot microservices.

    [root@docker-host ~]# docker run -it bartprokop/jirb /bin/bash
    root@f93e2a192f93:/# java -version
    java version "1.8.0_92"
    Java(TM) SE Runtime Environment (build 1.8.0_92-b14)
    Java HotSpot(TM) 64-Bit Server VM (build 25.92-b14, mixed mode)
    root@f93e2a192f93:/#

That's all folks.
