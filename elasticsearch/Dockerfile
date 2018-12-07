FROM docker.elastic.co/elasticsearch/elasticsearch:5.5.3

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch analysis-phonetic
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch analysis-icu

ADD config/elasticsearch.yml /usr/share/elasticsearch/config/
USER root
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
USER elasticsearch

