# Creating-Streaming-Data-Pipelines-using-Kafka
This is a simple project to create a data pipeline that collects the streaming data and loads it into a database.

# Scenario:

You are a data engineer at a data analytics consulting company. You have been assigned to a project that aims to de-congest the national highways by analyzing the road traffic data from different toll plazas. As a vehicle passes a toll plaza, the vehicle’s data like vehicle_id,vehicle_type,toll_plaza_id and timestamp are streamed to Kafka. Your job is to create a data pipe line that collects the streaming data and loads it into a database.

# Objectives
Create a streaming data pipe by performing these steps:
- Start a MySQL Database server.
- Create a table to hold the toll data.
- Start the Kafka server.
- Install the Kafka python driver.
- Install the MySQL python driver.
- Create a topic named toll in kafka.
- Download streaming data generator program.
- Customize the generator program to steam to toll topic.
- Download and customise streaming data consumer.
- Customize the consumer program to write into a MySQL database table.
- Verify that streamed data is being collected in the database table.

# Step 1: Preparation
wget https://archive.apache.org/dist/kafka/2.8.0/kafka_2.12-2.8.0.tgz
<img width="722" alt="image" src="https://github.com/kwagle7/Creating-Streaming-Data-Pipelines-using-Kafka/assets/13037108/967fc8c1-7221-4a8c-a518-4590c97b12a8">

# Start Zookeeper in a separate 
