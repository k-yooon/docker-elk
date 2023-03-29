ARG ELK_VERSION

FROM docker.elastic.co/kibana/kibana:${ELK_VERSION}
COPY plugin/opendistroAlertingKibana-1.13.0.0.zip /usr/share/plugin/opendistroAlertingKibana-1.13.0.0.zip
RUN bin/kibana-plugin install file:///usr/share/plugin/opendistroAlertingKibana-1.13.0.0.zip