FROM registry.access.redhat.com/ubi8/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/multi-version-example \
    USER_UID=1001 \
    USER_NAME=multi-version-example

# install operator binary
COPY build/_output/bin/multi-version-example ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
