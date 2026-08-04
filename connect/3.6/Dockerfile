ARG DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME
FROM $DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME/connect-base:3.6

LABEL maintainer="Debezium Community"

ENV DEBEZIUM_VERSION="3.6.1.Final" \
    MAVEN_REPO_CENTRAL="" \
    MAVEN_REPOS_ADDITIONAL="" \
    MONGODB_MD5=86c2987e543f2e5473d15e122d9afd3f \
    MYSQL_MD5=697381cccd7eed7cf7f0389cc7e8b888 \
    MARIADB_MD5=8e5cbd8e08747ab2656ca080ccb81a8b \
    POSTGRES_MD5=c0afa78a8b8f62a145950e827d582bda \
    SQLSERVER_MD5=17e7266d8440f179f56c7f8c783665c0 \
    ORACLE_MD5=6b6e9d811962299e9effd8786e567907 \
    DB2_MD5=6410a423568ec4ac0edefb8c3d5f423d \
    SPANNER_MD5=002d1b503e7880cde6f9f28c1057531a \
    VITESS_MD5=926f7f2aada0d1cf62f9fa8238abaad8 \
    JDBC_MD5=b56f763c3d7b9036183a79fb314f6a63 \
    INFORMIX_MD5=a1c1319a0eab2d44b840d9f55ca16c00 \
    IBMI_MD5=5caf1c3cba05a6e4ee1394cb5d30dad0 \
    COCKROACHDB_MD5=2131103a2f9cb0898a18c88644e8504e \
    SCRIPTING_MD5=d4bc82df6ebcfcb3c9261f81fe1a2678 \
    CHRONICLE_QUEUE_MD5=7d1935dc240eb72f45032d43815cbe68

RUN docker-maven-download debezium mongodb "$DEBEZIUM_VERSION" "$MONGODB_MD5" && \
    docker-maven-download debezium mysql "$DEBEZIUM_VERSION" "$MYSQL_MD5" && \
    docker-maven-download debezium mariadb "$DEBEZIUM_VERSION" "$MARIADB_MD5" && \
    docker-maven-download debezium postgres "$DEBEZIUM_VERSION" "$POSTGRES_MD5" && \
    docker-maven-download debezium sqlserver "$DEBEZIUM_VERSION" "$SQLSERVER_MD5" && \
    docker-maven-download debezium oracle "$DEBEZIUM_VERSION" "$ORACLE_MD5" && \
    docker-maven-download debezium jdbc "$DEBEZIUM_VERSION" "$JDBC_MD5" && \
    docker-maven-download debezium-additional db2 db2 "$DEBEZIUM_VERSION" "$DB2_MD5" && \
    docker-maven-download debezium-additional spanner spanner "$DEBEZIUM_VERSION" "$SPANNER_MD5" && \
    docker-maven-download debezium-additional vitess vitess "$DEBEZIUM_VERSION" "$VITESS_MD5" && \
    docker-maven-download debezium-additional informix informix "$DEBEZIUM_VERSION" "$INFORMIX_MD5" && \
    docker-maven-download debezium-additional ibmi ibmi "$DEBEZIUM_VERSION" "$IBMI_MD5" && \
    docker-maven-download debezium-additional cockroachdb cockroachdb "$DEBEZIUM_VERSION" "$COCKROACHDB_MD5" && \
    docker-maven-download debezium-optional scripting "$DEBEZIUM_VERSION" "$SCRIPTING_MD5" && \
    docker-maven-download debezium-store storage-chronicle-queue "$DEBEZIUM_VERSION" "$CHRONICLE_QUEUE_MD5"

