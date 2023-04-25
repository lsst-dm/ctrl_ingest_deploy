ARG LSST_STACK_VERSION
FROM lsstsqre/centos:${LSST_STACK_VERSION}

USER root
RUN yum install -y nc lldb

USER lsst
RUN source /opt/lsst/software/stack/loadLSST.bash && \
    pip install confluent_kafka==${CONFLUENT_KAFKA_VERSION}

ENTRYPOINT [ "/usr/bin/tail", "-f", "/dev/null" ]
