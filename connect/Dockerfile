FROM confluentinc/cp-kafka-connect-base:7.0.1

RUN confluent-hub install --no-prompt debezium/debezium-connector-mysql:1.7.1 && \
    confluent-hub install --no-prompt debezium/debezium-connector-mongodb:1.7.1 && \
    confluent-hub install --no-prompt confluentinc/kafka-connect-jdbc:10.3.1 && \
    confluent-hub install --no-prompt confluentinc/connect-transforms:latest

# custom sink
COPY kafka-connect-rest-plugin-1.0.3-shaded.jar /usr/share/java/
