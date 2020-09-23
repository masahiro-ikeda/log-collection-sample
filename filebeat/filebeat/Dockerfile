FROM docker.elastic.co/beats/filebeat:7.2.0

USER root
COPY ./usr/share/filebeat/filebeat.yml /usr/share/filebeat/filebeat.yml
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml

USER filebeat
RUN cd /usr/share/filebeat/
RUN filebeat modules enable nginx
RUN filebeat modules enable apache