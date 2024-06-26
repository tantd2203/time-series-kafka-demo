time-series-kafka-demo
============

![img](assets/cartoon-csv-kafka.jpeg)

Usage
-------------------

Clone repo and cd into directory.

```
https://github.com/tantd2203/time-series-kafka-demo.git
cd time-series-kafka-demo
```

**Start the Kafka broker**

```
docker compose up 
```


**Start a consumer**

To start a consumer for printing all messages in real-time from the stream "my-stream":

```
python bin/processStream.py my-stream
```

**Produce a time series stream**

Send time series from data/data.csv to topic “my-stream”, and speed it up by a factor of 10.

```
python bin/sendStream.py data/data.csv my-stream --speed 10
```

**Shut down and clean up**

Stop the consumer with Return and Ctrl+C.

Shutdown Kafka broker system:

```
docker compose down
```