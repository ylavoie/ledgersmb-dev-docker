FROM        postgres:10
MAINTAINER  LedgerSMB  devel@lists.ledgersmb.org

RUN DEBIAN_FRONTEND="noninteractive" apt-get -y update && \
    apt-get -y install postgresql-10-pgtap && \
    apt-get -y autoremove && \
    apt-get -y autoclean && \
    rm -rf /var/lib/apt/lists/* && \
    mkdir -p /docker-entrypoint-initdb.d

COPY lsmb-dev-init.sh /docker-entrypoint-initdb.d/lsmb-dev-init.sh

