# staffagent PY

Rename .env-dev to .env and update the values with your credentials

In terminal:

```bash
1. docker-compose up -d --build
2. docker-compose logs -f data_extractor # to view logs of the data_extractor
3. docker-compose up -d --force-recreate data_extractor # to restart the data_extractor
4. docker-compose exec kafka kafka-topics --create --topic data_extractor --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3
5. docker-compose exec kafka kafka-topics --bootstrap-server localhost:9092 --alter --topic data_extractor --partitions 5 # to increase the partitions of the topic
6. docker-compose up -d --scale data_extractor=3 # to scale the data_extractor containers to 3

```


docker-compose exec kafka kafka-topics  --bootstrap-server   localhost:9092 --delete --topic data_extractor 
