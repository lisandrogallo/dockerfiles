FROM elasticsearch:5
MAINTAINER lisogallo
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch ingest-attachment
EXPOSE 9200/tcp 9300/tcp
