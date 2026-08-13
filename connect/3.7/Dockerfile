ARG DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME
FROM $DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME/connect-base:3.7

LABEL maintainer="Debezium Community"

ENV DEBEZIUM_VERSION="3.7.0.Alpha2" \
    MAVEN_REPO_CENTRAL="" \
    MAVEN_REPOS_ADDITIONAL="" \
    MONGODB_MD5=c721ef7032827db2b25d9be701e55ecd \
    MYSQL_MD5=39c4af7bd4a4d50e24f564f94eb4783c \
    MARIADB_MD5=61aa167447dd2aee955446a140be43e6 \
    POSTGRES_MD5=7edb19464e27fdb08ffedba4c7bbe8b8 \
    SQLSERVER_MD5=bf0667fc6b6b3aaa8f0892b2e371ee42 \
    ORACLE_MD5=e333a9e9e8d8f415ab2fe11f262b2e92 \
    DB2_MD5=011affa219ec666af35886c322a2b769 \
    SPANNER_MD5=b566fbdbda6a3553318519a8c9f5770a \
    VITESS_MD5=49d72cabf747159c182ce4529b50372c \
    JDBC_MD5=b7c7b25f0815d7f3b838e79f894e6197 \
    INFORMIX_MD5=7c52c0fc750ced682a77aaba3db94ff8 \
    IBMI_MD5=48690bde5f66fef5788f869df13c4224 \
    COCKROACHDB_MD5=9883c5a00432456e2d241b4f02780072 \
    SCRIPTING_MD5=2b4de6cb405e0b9a567dd084baff3e6f \
    CHRONICLE_QUEUE_MD5=4879777f6bb06e7f562c93dc814e5cf0

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

