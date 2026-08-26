ARG DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME
FROM $DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME/connect-base:3.7

LABEL maintainer="Debezium Community"

ENV DEBEZIUM_VERSION="3.7.0.Beta1" \
    MAVEN_REPO_CENTRAL="" \
    MAVEN_REPOS_ADDITIONAL="" \
    MONGODB_MD5=0e8c7d537e1d46cfee1ea531b9fda0a5 \
    MYSQL_MD5=e1f4f0e5889ba8061d21af72418762bb \
    MARIADB_MD5=e7fc4a2f376c2ff04da04fac3e91cfda \
    POSTGRES_MD5=99cc7de2c9b15ce30c817e74aab4a6cd \
    SQLSERVER_MD5=f25ae59cdb0fe0f0fb91da975a472d6b \
    ORACLE_MD5=0fa38b63962c4e2c458ced62afd63c33 \
    DB2_MD5=338046bb10dbad87b184ffad09ca6e65 \
    SPANNER_MD5=d38291b521e491996693f7a466affa0c \
    VITESS_MD5=846ee3beec0f1924a44b249219ee8914 \
    JDBC_MD5=925a826f2f2feb8ca773f036a065e1a5 \
    INFORMIX_MD5=89e38417f1fb0f806b914ddd60bb8d8e \
    IBMI_MD5=bf94a5b7b67408610f56295bb7a16279 \
    COCKROACHDB_MD5=b713c58fbb976b650111abf44ddd23e8 \
    SCRIPTING_MD5=7795b25b1d7a2621da8d88b522704461 \
    CHRONICLE_QUEUE_MD5=cfb4a7f77726181bf95d20992cbeaab7

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

