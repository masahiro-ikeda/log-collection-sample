FROM docker.elastic.co/beats/filebeat:7.2.0

USER root
COPY ./usr/share/filebeat/filebeat.yml /usr/share/filebeat/filebeat.yml
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml && \
    yum -y update && \
    yum install -y unzip && \
    yum clean all

USER filebeat
RUN cd /usr/share/filebeat/ && \
    filebeat modules enable nginx && \
    filebeat modules enable apache