FROM    java:8

ENV SOLR_VERSION 3.6.2
ENV SOLR solr-$SOLR_VERSION
ENV SOLR_USER solr

RUN export DEBIAN_FRONTEND=noninteractive && \
  apt-get update && \
  apt-get -y install \
    curl \
    lsof \
    procps && \
  groupadd -r $SOLR_USER && \
  useradd -r -g $SOLR_USER $SOLR_USER && \
  mkdir -p /opt && \
  wget -nv --output-document=/opt/$SOLR.tgz http://archive.apache.org/dist/lucene/solr/$SOLR_VERSION/$SOLR.tgz && \
  tar -C /opt --extract --file /opt/$SOLR.tgz && \
  rm /opt/$SOLR.tgz && \
  ln -s /opt/$SOLR /opt/solr && \
  chown -R $SOLR_USER:$SOLR_USER /opt/solr /opt/$SOLR
EXPOSE 8983
WORKDIR /opt/solr
USER root
COPY ./myindex /opt/solr/server/solr/myindex
RUN chown -R solr:solr /opt/solr/server/solr/myindex
USER $SOLR_USER
CMD ["/bin/bash","-c" ,"/opt/solr/bin/solr -m 1g -f"]
