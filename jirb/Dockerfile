FROM debian

MAINTAINER Bart Prokop <prokop.bart@gmail.com>

ADD opt.tar.gz /

ENV JAVA_HOME="/opt/jdk1.8.0_101" \
    PATH=/opt/jdk1.8.0_101/bin:/opt/jruby-9.1.2.0/bin:$PATH

CMD ["jirb"]
