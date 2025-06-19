# BI-PROJECT

This is the final project of BI course.



### How to get started?

```bash
# zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties

# kafka
bin/kafka-server-start.sh config/server.properties

# flume
bin/flume-ng agent --conf conf --conf-file job/flume-kafka.conf --name agent -Dflume.root.logger=INFO,console

# fastapi
uvicorn app:app --host 0.0.0.0 --port 8000
```

最后启动消费者脚本




### Other command

```bash
# 创建topic
bin/kafka-topics.sh --create --topic click_logs --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1

# 删除topic
bin/kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic click_logs

# 查看topic
bin/kafka-topics.sh --bootstrap-server localhost:9092 --list
```