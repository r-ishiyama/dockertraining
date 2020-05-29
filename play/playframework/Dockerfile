FROM centos:7
RUN yum update -y
RUN yum install -y java-1.8.0-openjdk
RUN yum install -y java-1.8.0-openjdk-devel
RUN yum install -y curl
RUN yum install -y gnupg
RUN curl https://bintray.com/sbt/rpm/rpm > bintray-sbt-rpm.repo
RUN mv bintray-sbt-rpm.repo /etc/yum.repos.d/;yum install -y sbt
COPY frtraining/ /opt/frtraining
RUN cd opt/frtraining;sbt compile
CMD cd opt/frtraining; sbt run
