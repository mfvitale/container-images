ARG DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME
FROM $DEBEZIUM_DOCKER_REGISTRY_PRIMARY_NAME/connect-base:3.7

LABEL maintainer="Debezium Community"

ENV DEBEZIUM_VERSION="3.7.0.Alpha1" \
    MAVEN_REPO_CENTRAL="" \
    MAVEN_REPOS_ADDITIONAL="" \
    MONGODB_MD5=218aebae0fece55927ac5fbdbdc2e220 \
    MYSQL_MD5=19eab32594b5f5456d63acf10f3e571c \
    MARIADB_MD5=27a5efd3dd03aaf0f2100a86c41cdc83 \
    POSTGRES_MD5=5f84d2ba44302f8ee1614dbd64aad248 \
    SQLSERVER_MD5=dd2cd9d2372e77747125daea3911015e \
    ORACLE_MD5=73201b74b545f9624df72bef994c4d82 \
    DB2_MD5=e085b9acf54eed0bc5169e9e2abe9d11 \
    SPANNER_MD5=63f7d759517b3829d1e625e81b3a9978 \
    VITESS_MD5=cec0fd5dd4d9a7442436961e011b5f1e \
    JDBC_MD5=67f45c912b6ec1440cd051c83906c520 \
    INFORMIX_MD5=14a9b9723951d35d74ff6fed6c292de5 \
    IBMI_MD5=3094975282099b25cc8ecc757b844d04 \
    COCKROACHDB_MD5=58331e6b1ca2be07bd32b09643accc4a \
    SCRIPTING_MD5=b8ff224aa55d39b3b996025972eae301 \
    CHRONICLE_QUEUE_MD5=e19ed1846e7e8ba7c57b07af9f4f3aad

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

