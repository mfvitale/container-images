ARG DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME
FROM $DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME/connect-base:3.6

LABEL maintainer="Debezium Community"

ENV DEBEZIUM_VERSION="3.6.0.Final" \
    MAVEN_REPO_CENTRAL="" \
    MAVEN_REPOS_ADDITIONAL="" \
    MONGODB_MD5=f1188bbd0e978250da7378be194be40e \
    MYSQL_MD5=60020b9d7e6cc6278ebed8d772234859 \
    MARIADB_MD5=e7dd541c1e0798efa6b23e596c3ff367 \
    POSTGRES_MD5=e89e44ce9fa25d8a49693bb5774c194b \
    SQLSERVER_MD5=f55df5fce5e67ddf9538e13241ed527b \
    ORACLE_MD5=723a20c2bcf01dec3d3e005762ad2191 \
    DB2_MD5=4c350c1e3853421a3a945c3af9fc58fc \
    SPANNER_MD5=56dec76771e7dc43d43bceaa674c7522 \
    VITESS_MD5=862eda4a970c005e9a718d92aaf0cdee \
    JDBC_MD5=c658235613a004246ec78059af45db6a \
    INFORMIX_MD5=e8cdf31a7d401cd881159247f200847c \
    IBMI_MD5=e2080a5b4d60ca255d24e93df1919a12 \
    COCKROACHDB_MD5=5dbbe12ba26f0f68f2285a29302232a7 \
    SCRIPTING_MD5=1372ee715efc6f562f1a9cbbfff2d0f1 \
    CHRONICLE_QUEUE_MD5=1fb066da6a67c7c02962f59b4b8cd1ee

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

