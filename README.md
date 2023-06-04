# DynamicCryptoDataPipelineUsingKafka
For the purpose of creating and consuming scraped data, I am utilising a confluent Kafka cluster.In this project, I've built a real-time data pipeline that makes use of Kafka to scrape, analyse, and load data in JSON format onto S3.

Using a producer-consumer architecture to guarantee that the data is formatted correctly for loading onto S3 by making small changes as 
However, I didn't stop there; I also created a schema catalogue by crawling the data with AWS crawler. This catalogue is used by Athena, which enables me to perform straight S3 queries without first loading the data. 

Because of this, I can analyse the data much more quickly and save time and resources.I've also used Snowpipe to link S3 and Snowflake. A SNS notice is delivered to Snowpipe as soon as data is stored onto S3, and Snowpipe then begins loading the data into Snowflake automatically. This streamlines and automates the data loading process, freeing up time for other crucial duties.

![kafka_proj](https://user-images.githubusercontent.com/128234000/235583169-ae099338-60e4-4c04-a4fb-b4707a6e743a.png)
