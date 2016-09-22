FROM elasticsearch:2
MAINTAINER lisogallo
RUN /usr/share/elasticsearch/bin/plugin install --batch royrusso/elasticsearch-HQ
RUN /usr/share/elasticsearch/bin/plugin install --batch mapper-attachments
EXPOSE 9200/tcp 9300/tcp
