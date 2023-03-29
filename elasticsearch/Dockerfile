ARG ELK_VERSION

FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

RUN elasticsearch-plugin install analysis-nori
COPY plugin/jaso-analyzer-plugin-7.10.2-plugin.zip /usr/share/plugin/jaso-analyzer-plugin-7.10.2-plugin.zip
RUN bin/elasticsearch-plugin install -b file:///usr/share/plugin/jaso-analyzer-plugin-7.10.2-plugin.zip
COPY plugin/alerting.zip /usr/share/plugin/alerting.zip
RUN bin/elasticsearch-plugin install -b file:///usr/share/plugin/alerting.zip
