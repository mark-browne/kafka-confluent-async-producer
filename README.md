
## produce:
java -jar build/libs/kafka-producer-application-standalone-0.0.1.jar configuration/dev.properties input.txt


## consume messages:
```
docker exec --interactive --tty broker \
kafka-console-consumer --bootstrap-server broker:9092 \
                       --topic output-topic \
                       --from-beginning